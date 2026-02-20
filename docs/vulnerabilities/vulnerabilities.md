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

# 🎭 Encoding and Obfuscation

> **The "Art of Disguise":** If an attacker can change the pattern of a command without changing its meaning, the WAF fails to detect it.


### 🛡️ The Pattern-Matching Problem
Web Application Firewalls (WAFs) act as gatekeepers, scanning incoming traffic for known "bad words" or signatures, such as:
* `SELECT` or `UNION` (SQL Injection)
* `<script>` (Cross-Site Scripting)
* `../` (Path Traversal)

Attackers win by making these "bad words" unrecognizable to the WAF while ensuring they remain perfectly executable for the back-end.

### 🛠️ Common Techniques

| Technique | How it Works | Example |
| :--- | :--- | :--- |
| **URL Encoding** | Replaces characters with `%` followed by their ASCII hex equivalent. | `SELECT` becomes `%53%45%4c%45%43%54` |
| **Hex/Unicode** | Uses different character sets that the back-end might decode but the WAF ignores. | `<` becomes `\u003c` |
| **Double Encoding** | Encoding a character twice (e.g., `%2527`) to bypass WAFs that only perform one round of decoding. | `'` → `%27` → `%2527` |
| **Comment Injection** | Inserting "noise" that the WAF sees as text but the Database ignores. | `SEL/*comment*/ECT` |


### ⚠️ The Vulnerability: The "Language Gap"
The danger occurs when the **WAF** and the **Back-end** don't "speak" the same encoding language. 

1. **The WAF** scans the encoded string, doesn't recognize the "bad word," and marks it as **SAFE**.
2. **The Back-end** receives the string, decodes it back to the original malicious command, and **EXECUTES** it.

> **Key Takeaway:** A WAF is only as good as its decoding engine. If it can't "unmask" the disguise, the malicious command slips right through.

## 📜 The Background: Why Encoding Exists

In the early days of the internet, systems were fragile. If you tried to send a "space" character or a "quote" in a URL, it would break the connection or confuse the server. 


To fix this, **RFC 3986** (and others) created standard ways to "package" special characters so they could travel safely across the wire. This is called **Encoding**.


### 🔍 The Core Vulnerability: Interpretation

The vulnerability isn't in the encoding itself; it’s in the **Interpretation**. 

> **The Customs Officer Analogy** 🛂
> A WAF is like a customs officer reading a passport. If the passport is written in a language the officer doesn't speak fluently (like an obscure **Unicode** variant), they might let it pass. However, if the person at the **destination** (the back-end) *does* speak it, the "smuggled" message gets through.


### ⚠️ Why It Bypasses Security
1. **The WAF** scans the traffic for "bad words" (like `SELECT` or `<script>`).
2. **The Attacker** disguises those words using encoding the WAF isn't configured to decode.
3. **The Back-end** is often more "intelligent" or flexible, decoding the payload and executing the malicious command after it has already cleared the gatekeeper.