# Vulnerabilities In WAF's

# 🍕 HTTP Request Smuggling

> **Definition:** HTTP Request Smuggling is the digital equivalent of two people sharing a pizza but having different rules about what counts as a "slice." It exploits the discrepancy in how a chain of servers (Front-end vs. Back-end) interprets request boundaries.


## 🔍 The Root Cause: The "Length" Conflict

Modern web infrastructure uses two different methods to define the size of an HTTP message. Vulnerabilities occur when these two methods conflict:

* **Content-Length (CL):** A simple number in bytes (e.g., `Content-Length: 11`).
* **Transfer-Encoding (TE):** Uses "chunked" encoding where the message is sent in blocks, ending with a specific `0` chunk.


## 🛠️ Detailed Example: The CL.TE Attack

In this scenario, the **Front-end** uses `Content-Length` while the **Back-end** uses `Transfer-Encoding`.

### 1. The Malicious Request
An attacker sends a request containing both headers:

```http
POST / HTTP/1.1
Host: vulnerable-website.com
Content-Length: 13
Transfer-Encoding: chunked

0

SMUGGLED
```

### 2. Server Processing Discrepancy

When the request reaches the infrastructure, the two servers interpret the data stream differently:

| Server | Header Used | Action |
| :--- | :--- | :--- |
| **Front-end** | `Content-Length: 13` | Counts 13 bytes (up to "SMUGGLED"), considers it one complete request, and forwards it. |
| **Back-end** | `Transfer-Encoding: chunked` | Sees the `0` (end of chunk), stops processing the current request, and leaves `SMUGGLED` in the memory buffer. |

> **Result:** The `SMUGGLED` payload remains "stuck" at the beginning of the Back-end's request queue, waiting to be prepended to the very next request that arrives.


The vulnerability stems from the fact that the two servers are following different sets of rules for the exact same data stream.

### 3. The Front-end's Perspective
The Front-end server is configured to prioritize the **`Content-Length`** header.
* **The Logic:** It sees `Content-Length: 13`.
* **The Action:** It counts 13 bytes (starting from the first `0` down to the end of the word `SMUGGLED`).
* **The Conclusion:** It thinks, *"Okay, this is one complete, valid request,"* and forwards the entire packet to the back-end.


### 4. The Back-end's Perspective
The Back-end server is configured to prioritize the **`Transfer-Encoding: chunked`** header.
* **The Logic:** In chunked encoding, a `0` followed by a blank line (CRLF) signifies the absolute end of an HTTP request.
* **The Action:** The Back-end processes the request up to the `0`, assumes it has reached the end, and stops.
* **The Consequence:** It leaves the remaining 8 bytes (`SMUGGLED`) sitting unprocessed in its **memory buffer**.


> **The Result:** We now have a "poisoned" buffer. The next request to arrive at the Back-end will have `SMUGGLED` automatically prepended to its start.

### 5. The Victim's Request

While the smuggled data is sitting in the back-end's buffer, an innocent user sends a standard, legitimate request:

```
GET /home HTTP/1.1
Host: vulnerable-website.com
```