# 🛡️ VigilantEdge
> An Autonomous AI-Driven Web Application Firewall for Adaptive, Self-Healing, and Zero-Day Threat Defense

## 🧱 VigilantEdge — AI-Driven Adaptive Web Application Firewall

Modern web applications, **cloud-native platforms**, and **API-centric architectures** are increasingly exposed to sophisticated cyber threats, including **zero-day exploits**, **automated attacks**, and **adversarial behaviors** that bypass traditional **rule-based Web Application Firewalls (WAFs)**. Conventional WAF solutions rely heavily on **static signatures** and **manually defined rules**, making them ineffective against evolving attack patterns and resulting in **high false-positive rates**.

**VigilantEdge** is an **intelligent, AI-driven Web Application Firewall** designed to provide **adaptive, autonomous, and resilient security** for **web and API-based systems**. The project focuses on transforming the WAF from a **static perimeter defense mechanism** into a **learning security system** capable of detecting, analyzing, and responding to **both known and unknown threats in real time**.

The proposed system operates as a **reverse-proxy-based security layer** that continuously inspects incoming **HTTP and API traffic**. It employs **behavioral analysis** and **machine learning–based anomaly detection** to model normal user and application behavior and identify deviations indicative of malicious activity. Unlike traditional signature-based approaches, VigilantEdge emphasizes **behavioral patterns**, **request sequencing**, **payload characteristics**, and **traffic anomalies**, enabling early detection of **zero-day and logic-based attacks**.

To enhance defensive adaptability, VigilantEdge integrates **AI-assisted rule optimization**, where firewall policies are **dynamically refined** based on observed attack outcomes and feedback from security decisions. This reduces **manual configuration effort** and minimizes **false positives** while maintaining robust protection. The system further incorporates **controlled AI red teaming** and **automated penetration testing** within an **isolated environment**, allowing the firewall to continuously evaluate its own effectiveness, learn from **simulated adversarial behavior**, and strengthen detection logic proactively.

A key architectural contribution of VigilantEdge is its **self-healing security mechanism**, which enables **automated mitigation actions** such as **rule updates**, **temporary access restrictions**, and **configuration restoration** in response to detected threats. The framework aligns with **Zero Trust security principles**, enforcing **continuous verification** of requests rather than assuming trust based on network location.

To support **transparency and compliance**, VigilantEdge employs **Explainable Artificial Intelligence (XAI)** techniques that provide **interpretable insights** into security decisions, making the system suitable for **regulatory and audit requirements**. The overall design prioritizes **scalability**, **modularity**, and **extensibility**, allowing future integration of **global threat intelligence**, **decentralized learning**, and **advanced deception mechanisms**.

By combining **adaptive detection**, **autonomous response**, and **continuous learning**, VigilantEdge demonstrates a shift from **reactive web security** toward a **proactive and intelligent defense model**, offering a practical foundation for **next-generation web application protection**.

## 📁 Repository Structure

```text
│── README.md                     # Project overview, architecture, and usage
│── requirements.txt              # Python dependencies for the entire system
│
├── AI_engine/                    # Core AI and learning components
│   ├── anomaly_detection/        # Behavioral modeling and anomaly detection models
│   ├── explainability/           # Explainable AI (XAI) modules for decision transparency
│   ├── red_teaming/              # AI-driven red teaming and adversarial learning logic
│   └── zero_day_simulation/      # Simulation of zero-day and unknown attack patterns
│
├── config/                       # Centralized configuration management
│   ├── model_params.yaml         # ML model hyperparameters and tuning settings
│   ├── system.yaml               # Global system configuration and modes
│   └── thresholds.yaml           # Security thresholds and risk scoring limits
│
├── core/                         # Decision-making and trust evaluation logic
│   ├── decision_engine/          # Final security decision and action selection
│   ├── normalizer/               # Request normalization and feature standardization
│   ├── threat_scoring/           # Risk scoring and threat severity computation
│   └── trust_engine/             # Zero Trust evaluation and continuous verification
│
├── data/                         # Data storage and processing pipeline
│   ├── features/                # Extracted feature vectors for ML models
│   ├── processed/               # Cleaned and preprocessed datasets
│   └── raw/                     # Raw logs, traffic samples, and request data
│
├── docs/                         # Documentation and research artifacts
│   ├── architecture/            # System architecture diagrams and design docs
│   ├── compliance/              # GDPR, ISO 27001, NIST, and regulatory mappings
│   └── research/                # Research notes, experiments, and paper drafts
│
├── ingestion/                   # Traffic and data ingestion layer
│   ├── log_collector/           # Collection of access logs and request traces
│   ├── proxy/                   # Reverse-proxy implementation (HTTP/API inspection)
│   └── schema/                  # Request/response schemas and validation logic
│
├── response_engine/             # Automated response and mitigation actions
│   ├── deception/               # Deception mechanisms (honeypots, fake endpoints)
│   ├── mitigation/              # Blocking, rate-limiting, and access control actions
│   ├── rule_optimization/       # AI-assisted firewall rule refinement
│   └── self_healing/             # Automated recovery and configuration restoration
│
├── scripts/                     # Utility and operational scripts
│   ├── run_pipeline.sh          # Launches the complete VigilantEdge pipeline
│   ├── setup_env.sh             # Environment setup and dependency installation
│   └── simulate_attack.py       # Attack simulation for testing and validation
│
├── security/                    # Cryptographic and secret management components
│   ├── auth/                    # Authentication and identity verification logic
│   ├── crypto/                  # Cryptographic primitives and secure operations
│   └── secrets/                 # Secure storage for keys, tokens, and credentials
│
├── soc_interface/               # Security Operations Center (SOC) integration
│   ├── alerts/                  # Alert generation and incident notifications
│   ├── copilot/                 # AI-assisted SOC analyst support tools
│   └── dashboard/               # Monitoring and visualization dashboards
│
└── tests/                       # Testing and validation suite
    ├── adversarial_tests/       # Tests against adaptive and intelligent attackers
    ├── attack_simulations/      # Simulated attack scenarios and replay tests
    └── performance_tests/       # Load, latency, and scalability testing
```

## 📁 VigilantEdge Directory Bootstrap (Architecture-Aligned Layout)

The following directory structure initializes the complete **VigilantEdge project layout**, covering **AI security intelligence**, **traffic ingestion**, **decision-making core**, **response automation**, **SOC integration**, **security primitives**, **testing**, and **research documentation**.

This structure is created using a single Windows command sequence (`mkdir`) to ensure a **consistent, reproducible, and architecture-aligned project setup**.

```bat
VigilantEdge\docs\architecture ^
VigilantEdge\docs\compliance ^
VigilantEdge\docs\research ^
VigilantEdge\ingestion\reverse_proxy ^
VigilantEdge\ingestion\api_gateway ^
VigilantEdge\ingestion\schema ^
VigilantEdge\core\normalizer ^
VigilantEdge\core\trust_engine ^
VigilantEdge\core\threat_scoring ^
VigilantEdge\core\decision_engine ^
VigilantEdge\ai_engine\anomaly_detection ^
VigilantEdge\ai_engine\zero_day_detection ^
VigilantEdge\ai_engine\red_teaming ^
VigilantEdge\ai_engine\explainability ^
VigilantEdge\response_engine\mitigation ^
VigilantEdge\response_engine\self_healing ^
VigilantEdge\response_engine\deception ^
VigilantEdge\response_engine\rule_optimization ^
VigilantEdge\soc_interface\backend ^
VigilantEdge\soc_interface\frontend\dashboard ^
VigilantEdge\soc_interface\frontend\charts ^
VigilantEdge\soc_interface\copilot ^
VigilantEdge\security\crypto ^
VigilantEdge\security\auth ^
VigilantEdge\security\secrets ^
VigilantEdge\data\raw ^
VigilantEdge\data\processed ^
VigilantEdge\data\features ^
VigilantEdge\tests\attack_tests ^
VigilantEdge\tests\adversarial_tests ^
VigilantEdge\tests\load_tests ^
VigilantEdge\scripts ^
VigilantEdge\config
```

## 🧱 Initial File Scaffold Setup

The following commands initialize **core project files** required for configuration, automation, documentation, and execution of the VigilantEdge system.

These files act as **placeholders and entry points**, ensuring a clean, consistent structure before implementation begins.

```bat
type nul > VigilantEdge\docs\architecture\system_architecture.md
type nul > VigilantEdge\docs\architecture\component_diagram.md
type nul > VigilantEdge\docs\architecture\data_flow.md
type nul > VigilantEdge\docs\architecture\trust_boundaries.md

type nul > VigilantEdge\docs\compliance\gdpr.md
type nul > VigilantEdge\docs\compliance\iso27001.md
type nul > VigilantEdge\docs\compliance\nist.md

type nul > VigilantEdge\docs\research\abstract.md
type nul > VigilantEdge\docs\research\methodology.md
type nul > VigilantEdge\docs\research\experiments.md
type nul > VigilantEdge\docs\research\future_work.md

type nul > VigilantEdge\ingestion\reverse_proxy\nginx.conf
type nul > VigilantEdge\ingestion\reverse_proxy\traffic_forwarder.py
type nul > VigilantEdge\ingestion\api_gateway\auth_middleware.py
type nul > VigilantEdge\ingestion\api_gateway\rate_limiter.py
type nul > VigilantEdge\ingestion\schema\event_schema.json

type nul > VigilantEdge\core\normalizer\normalize.py
type nul > VigilantEdge\core\trust_engine\zero_trust.py
type nul > VigilantEdge\core\threat_scoring\scoring.py
type nul > VigilantEdge\core\decision_engine\orchestrator.py

type nul > VigilantEdge\ai_engine\anomaly_detection\isolation_forest.py
type nul > VigilantEdge\ai_engine\anomaly_detection\one_class_svm.py
type nul > VigilantEdge\ai_engine\anomaly_detection\baseline_training.py
type nul > VigilantEdge\ai_engine\zero_day_detection\behavior_sequence_model.py
type nul > VigilantEdge\ai_engine\red_teaming\attack_simulator.py
type nul > VigilantEdge\ai_engine\explainability\shap_explainer.py
type nul > VigilantEdge\ai_engine\explainability\lime_explainer.py

type nul > VigilantEdge\response_engine\mitigation\firewall_update.py
type nul > VigilantEdge\response_engine\mitigation\rate_blocker.py
type nul > VigilantEdge\response_engine\self_healing\config_rollback.py
type nul > VigilantEdge\response_engine\self_healing\auto_patch.py
type nul > VigilantEdge\response_engine\deception\honeytokens.py
type nul > VigilantEdge\response_engine\deception\fake_endpoints.py
type nul > VigilantEdge\response_engine\rule_optimization\adaptive_rules.py

type nul > VigilantEdge\soc_interface\backend\soc_api.py
type nul > VigilantEdge\soc_interface\copilot\ai_assistant.py

type nul > VigilantEdge\security\crypto\key_manager.py
type nul > VigilantEdge\security\auth\jwt_auth.py
type nul > VigilantEdge\security\secrets\vault_adapter.py

type nul > VigilantEdge\scripts\setup_env.sh
type nul > VigilantEdge\scripts\start_system.sh
type nul > VigilantEdge\scripts\simulate_attack.py

type nul > VigilantEdge\config\system.yaml
type nul > VigilantEdge\config\thresholds.yaml
type nul > VigilantEdge\config\models.yaml

type nul > VigilantEdge\requirements.txt
type nul > VigilantEdge\README.md
```

## 🏗 VigilantEdge – Unified Technology Architecture

> Explore the core technologies used in this application. Below, you’ll find a detailed list of our frameworks and libraries, along with insights into why they were the right fit for our goals.

## 🧱 LAYER 1 – Network & Traffic Control Layer

⚪ The **Network & Traffic Control Layer** is the **entry point** of VigilantEdge.

It intercepts traffic, applies first-line controls, terminates TLS, routes requests into the platform, and enforces **“edge” security policies** before heavy AI processing begins.

This ensures that only normalized, policy-compliant, and pre-filtered traffic is forwarded to the deeper intelligence layers of the system.

### 🔧Technologies Used:
1. Nginx
2. FastAPI
3. Uvicorn
4. Redis (edge rate-limit + fast blocking decisions)
5. Pydantic (strict schema validation at ingestion boundary)
6. Envoy (service proxy for advanced routing + mTLS hooks)

## 🤖 LAYER 2 – AI & Intelligence Engine

🟢 The **AI & Intelligence Engine Layer** is responsible for behavioral modeling, anomaly detection, zero-day analysis, and explainable security decisions.  
This layer transforms raw traffic data into actionable threat intelligence.

### 🔧Technologies Used:
1. NumPy
2. Pandas
3. Scikit-Learn
4. PyTorch
5. SHAP
6. LIME
7. NetworkX (attack graphs in code)
8. Neo4j (graph database for attribution + kill-chain mapping)
9. ART (Adversarial Robustness Toolbox) (adversarial ML testing)

## 🔐 LAYER 3 – Security & Zero Trust Layer

🟡 The **Security & Zero Trust Layer** ensures authenticated access, secure key management, and continuous trust verification across all VigilantEdge components.
This layer enforces cryptographic integrity, identity validation, and secret protection to align with **Zero Trust security principles**.

### 🔧Technologies Used:
1. cryptography (core encryption/signing primitives)
2. python-jose (JWT) (token handling)
3. Keycloak (OIDC/OAuth2) (enterprise identity, SSO, roles)
4. HashiCorp Vault (secrets + key lifecycle + rotation)
5. OPA (Open Policy Agent) (policy-as-code authorization)
6. mTLS stack: Envoy + cert-manager (service-to-service authentication)

## ⚙️ LAYER 4 – Autonomous Response Layer

🔴 The **Autonomous Response Layer** is responsible for executing real-time mitigation, adaptive rule enforcement, and self-healing actions based on decisions produced by the AI and core security engines.
This layer transforms detection into **automated defensive action**, minimizing manual intervention and reducing response latency.

### 🔧Technologies Used:
1. FastAPI orchestration (action APIs + orchestration)
2. Redis (fast enforcement decisions + cooldowns)
3. Custom Python Response Modules (mitigation, deception, rollback)
4. Ansible (repeatable remediation + patch automation)
5. Argo CD (GitOps) (restore known-good config via GitOps)

## 📊 LAYER 5 – SOC & Visualization Layer

🟣 The **SOC & Visualization Layer** provides real-time visibility, alerting, and human-in-the-loop interaction for security analysts.
This layer ensures that VigilantEdge not only detects and mitigates threats autonomously but also provides transparent monitoring, explainability, and operational control for Security Operations Center (SOC) teams.

## 🔧Technologies Used:
1. React
2. Recharts

## 🧪 LAYER 6 – Testing & Validation

🟢 The **Testing & Validation Layer** ensures the reliability, robustness, and security effectiveness of VigilantEdge under real-world and adversarial conditions.
This layer validates detection accuracy, response correctness, performance stability, and resilience against adaptive attackers.

## 🔧Technologies Used:
1. PyTest
2. Custom attack simulators

## 🧬 LAYER 7 – Event Streaming & Background Processing Layer

The **Event Streaming & Background Processing Layer** ensures VigilantEdge is truly **real-time and scalable**.

Instead of processing everything synchronously (which can drop events and slow down the gateway), this layer buffers traffic, streams events to multiple consumers, and executes heavy tasks asynchronously.

This architecture prevents bottlenecks in the ingestion layer and allows AI processing, analytics, and reporting to scale independently.

### 🔧Technologies:

1. Apache Kafka (event streaming backbone)
2. Kafka Connect (pipelines between Kafka ↔ OpenSearch/Postgres)
3. Celery (background jobs like scans, retraining, reporting)
4. RabbitMQ (reliable task queue broker for Celery)
5. APScheduler (scheduled security jobs, periodic tasks)

## 🧩 LAYER 8 – Detection Engineering Layer 

🟡 The **Detection Engineering Layer** adds rule-based and protocol-aware detection that complements machine learning models.

In real-world SOC systems, security never relies solely on ML. Instead, it combines **signatures + telemetry + rules + ML** to achieve high precision and operational reliability.

### 🔧Technologies Used:

1. Suricata (network IDS signatures + protocol metadata)
2. Zeek (deep network telemetry extraction)
3. YARA (payload/pattern matching engine)
4. Sigma Rules (standard rule format for detections)

## 🧬 LAYER 9 – Cryptography & Post-Quantum Security Layer 

🔵 The **Cryptography & Post-Quantum Security Layer** hardens VigilantEdge against current and future cryptographic threats.

This layer introduces modern, secure cryptographic primitives and supports post-quantum cryptography (PQC) experimentation to reinforce the platform’s long-term security posture.

It ensures that VigilantEdge is not only resilient against today’s threats but also prepared for emerging risks posed by quantum computing.

### 🔧Technologies Used:

1. cryptography (classical crypto foundation)
2. libsodium / PyNaCl (safe modern crypto APIs)
3. Open Quantum Safe (OQS) / oqs-provider (PQC algorithm experiments)

## 🗃️ LAYER 10 – Storage, Search & Analytics Layer 

🟠 The **Storage, Search & Analytics Layer** ensures that all security data is stored, indexed, and analyzed in a manner suitable for real-world SOC workflows.

Security platforms require more than simple log storage. This layer provides structured persistence, fast retrieval, searchable indexing, artifact management, and high-speed analytical processing.

### 🔧Technologies Used:
1. PostgreSQL (incidents, audit, RBAC, workflows)
2. Redis (cache + rapid enforcement state)
3. OpenSearch / Elasticsearch (SOC search engine over events/logs)
4. S3 / MinIO (datasets + model artifacts + large logs)
5. ClickHouse (high-speed time-series security analytics)

## 📈 LAYER 11 – Observability & Telemetry Layer

⚪ The **Observability & Telemetry Layer** proves that VigilantEdge operates reliably under load and provides full visibility across the security pipeline.

### 🔧Technologies Used:
1. Prometheus (metrics collection)
2. Grafana (dashboards)
3. OpenTelemetry (distributed traces)
4. Loki (platform/system log aggregation)

## 🧰 LAYER 12 – MLOps & Reproducibility Layer 

🟤 The **MLOps & Reproducibility Layer** ensures that VigilantEdge’s AI models are credible, repeatable, and production-ready.

Security AI must not be a black box. Every model must be reproducible, versioned, tracked, evaluated, and deployed in a controlled manner. This layer guarantees scientific rigor and operational reliability.

### 🔧Technologies Used:
1. MLflow (experiment tracking + model registry)
2. DVC (dataset version control)
3. ONNX (model export standard)
4. onnxruntime (optimized inference runtime)

## 🛡️ LAYER 13 – DevSecOps, Containerization & CI/CD Layer

⚫ The **DevSecOps & Deployment Layer** ensures that VigilantEdge is deployable, scalable, and continuously secured across environments.

This layer standardizes builds, scans container images, automates testing pipelines, and enables SOC-grade production deployments.

It bridges development, security, and operations into a unified workflow.

### 🔧Technologies Used:
1. Docker
2. Docker Compose
3. Kubernetes
4. Helm
5. GitHub Actions
6. Trivy (container vulnerability scanning)

## 🕵️ LAYER 14 – Threat Intelligence, OSINT & Dark Web Intelligence Layer 

The **Threat Intelligence, OSINT & Dark Web Intelligence Layer** enriches VigilantEdge detections with external and contextual threat knowledge.

This layer integrates structured intelligence feeds, Indicators of Compromise (IOCs), threat actor mappings, and campaign intelligence to provide context-aware security decisions.

Unlike isolated detection systems, VigilantEdge correlates internal anomalies with global intelligence sources to improve accuracy, reduce false positives, and detect coordinated attack campaigns.

### 🔧Technologies Used:

1. MISP (IOC and threat intel platform)
2. OpenCTI (threat knowledge graph)
3. STIX/TAXII tooling (standard threat intel formats + transport)

## 🌐 LAYER 15 – DASN: Federated Learning + Blockchain Trust Layer

The **Decentralized AI Security Network (DASN) Layer** enables collaborative defense across multiple deployments without centralizing sensitive data.

This layer introduces federated model training and tamper-proof intelligence sharing, allowing multiple VigilantEdge nodes to learn collectively while preserving data privacy.

Instead of aggregating raw logs into a central system, DASN ensures that models are trained locally and only model updates are shared securely.

### 🔧Technologies Used:
1. Flower (federated learning orchestration)
2. PySyft (privacy-preserving ML experiments)
3. Hyperledger Fabric (tamper-proof intel ledger + provenance)
4. Go (commonly used in high-perf agents and Fabric ecosystem tooling)

## 🧨 LAYER 16 – Automated Pentesting & Red Team Validation Layer

The **Automated Pentesting & Red Team Validation Layer** ensures that VigilantEdge is continuously tested against controlled attack scenarios in a secure lab environment.

This layer is strictly for defensive validation and security hardening. It is not designed for offensive or unauthorized use.

By integrating automated security testing tools, VigilantEdge can validate detection logic, response accuracy, and system resilience against evolving threats.

### 🔧Technologies Used:
1. OWASP ZAP (DAST testing for web apps)
2. Nuclei (template-based scanning for regression testing)
3. Semgrep (SAST)
4. Bandit (Python security linting)

# 🚦 Installation Strategy & Deployment Discipline

## 🛑 Rule #1: Do NOT Install Everything Directly on Your OS

For a complex, multi-layered security stack like VigilantEdge:

- Use **Docker** for infrastructure services  
- Use a **Python virtual environment (venv)** for application code  
- Keep the host operating system clean and minimal  

This prevents dependency conflicts, ensures reproducibility, and maintains long-term system stability.

# 📦 Official Installation Order (Follow Exactly)

The stack must be installed in the following phased sequence.

## 🧱 Phase 1 – Core Runtime

Install foundational tools first:

1. Python  
2. Node  
3. Git  
4. Docker  

These are prerequisites for almost every other component.

## 🗄 Phase 2 – Databases & Cache

Install storage and caching systems:

1. PostgreSQL  
2. Redis  
3. OpenSearch  

These provide transactional storage, caching, and indexed search capabilities.

## 📡 Phase 3 – Streaming Backbone

Install asynchronous processing infrastructure:

1. Kafka  
2. RabbitMQ  

These enable event streaming and distributed background processing.

## 📊 Phase 4 – Observability

Install monitoring and telemetry tools:

1. Prometheus  
2. Grafana  
3. Loki  

These track metrics, logs, and system performance.

## 🔐 Phase 5 – Security & Identity

Install identity and policy enforcement systems:

1. Keycloak  
2. Vault  
3. OPA (Open Policy Agent)  

These enforce authentication, secret management, and policy control.

## 🛡 Phase 6 – Detection & Intelligence Engines

Install detection and threat intelligence components:

1. Suricata  
2. Zeek  
3. YARA  
4. Neo4j  

These support network detection, rule scanning, artifact analysis, and attack graph storage.

## 🧠 Phase 7 – MLOps

Install model lifecycle and deployment tools:

1. MLflow  
2. DVC  
3. ONNX  

These ensure model versioning, reproducibility, and portable inference.

## 🛠 Phase 8 – DevSecOps

Install container orchestration and CI/CD tooling:

1. Kubernetes  
2. Helm  
3. Trivy  
4. GitHub Actions  

These enable scalable deployment and secure build pipelines.

## 🌍 Phase 9 – Advanced (Optional – After Core Stable)

Install only after core platform is stable:

1. MISP  
2. OpenCTI  
3. Flower  
4. Hyperledger  
5. OQS (Open Quantum Safe)  

These support threat intelligence sharing, federated learning, blockchain trust, and post-quantum cryptography experimentation.


## Why This Order Matters

- Prevents cascading dependency failures  
- Ensures base services are stable before advanced features  
- Supports incremental system validation  
- Keeps the host OS clean and controlled  

This phased approach transforms VigilantEdge from a chaotic stack into a **disciplined, production-grade security platform deployment**.

# 🪟 Windows Installation Order

⚠️ **Important:** Windows is not ideal for running Suricata and Zeek natively.  
The recommended approach is:

> **Windows + WSL2 (Ubuntu) + Docker Desktop**

This provides Linux compatibility while keeping a Windows development environment.

## 🔹 STEP 1 – Install Core Tools

Install the foundational tools in the exact order below:

1. **Git**
2. **Python 3.10+**
3. **Node.js (LTS version)**
4. **Docker Desktop**
5. **Enable WSL2 (Ubuntu recommended)**

### 📌 After Installation – Verify Setup

Run the following commands in PowerShell or CMD:

```powershell
python --version
node --version
docker --version
wsl --status
```

## 🔹 STEP 2 – Setup Python Environment

After installing core tools, create an isolated Python environment.

This ensures:
- Clean dependency management  
- No system-wide conflicts  
- Reproducible builds  

### 📌 Create Virtual Environment

```
python -m venv venv
venv\Scripts\activate
pip install --upgrade pip
```

## 🔹 STEP 3 – Install Core Python Libraries

After activating the virtual environment, install the required core libraries for VigilantEdge.

### 📌 Install Dependencies

```powershell
pip install fastapi uvicorn numpy pandas scikit-learn torch shap lime `
pydantic redis cryptography python-jose networkx mlflow dvc onnx onnxruntime `
pytest celery
```

## 🔹 STEP 3 – Run Infrastructure via Docker

Instead of installing infrastructure services directly on your OS, run them inside Docker containers.

```powershell
docker run -d `
  --name postgres `
  -p 5432:5432 `
  -e POSTGRES_PASSWORD=admin `
  postgres
  ```

### 🗄 PostgreSQL

```powershell
docker run -d `
  --name postgres `
  -p 5432:5432 `
  -e POSTGRES_PASSWORD=admin `
  postgres