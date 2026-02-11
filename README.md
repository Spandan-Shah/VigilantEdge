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