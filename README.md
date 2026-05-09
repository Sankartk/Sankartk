# Hi, I'm Sankar 👋

I'm Sankar, a backend and data engineer in Newark, DE. I work on the parts that don't make headlines but break everything when they fail — pipelines that never drop a message, reconciliation engines that explain their own breaks, APIs that make data actually usable. Lately I've been pushing AI into that same layer: LLMs that don't just flag anomalies but tell you why, agents that handle routine ops so no one gets paged at 2am.

🌐 **[sankartk.dev](https://sankartk.dev)** — architecture write-ups, live dashboards, and project deep-dives

---

## Projects

### 🟣 [FinFlow](https://sankartk.dev/projects/finflow) · [Repo](https://github.com/Sankartk/finflow)
AI-native reconciliation engine built end-to-end: Kafka ingestion with checkpoint replay, a five-pass matching pipeline (exact → timing tolerance → fuzzy reference → amount threshold → Ollama LLM), pgvector cosine search for anomaly memory across runs, and a Strawberry GraphQL API with a Streamlit ops dashboard. **94.2% auto-match rate across 2,000 transactions. Zero external API costs.**

`Python` `Kafka` `PostgreSQL` `pgvector` `Ollama` `FastAPI` `GraphQL` `Streamlit`

---

### 🔵 [Ops Copilot](https://sankartk.dev/projects/ops-copilot) · [Repo](https://github.com/Sankartk/ops-copilot-bedrock)
FAISS-indexed runbook retrieval feeding a Bedrock remediation plan through a Step Functions approval gate — answers cite exact file and line number, nothing runs on production without explicit human sign-off. Swap one env var to go from Ollama local to AWS Bedrock.

`Python` `FAISS` `AWS Bedrock` `Step Functions` `Lambda` `SNS` `SAM` `Streamlit`

---

### 🟢 [CashCast](https://sankartk.dev/projects/cashcast) · [Repo](https://github.com/Sankartk/cashcast)
Per-branch vault cash demand forecasting: Ridge Regression model per branch trained on 730 days of history, Isolation Forest for anomaly flags, 14-day forward horizon — **avg MAPE 9.1%**. Turns the standard 15–20% buffer guess into a data-backed order recommendation with confidence bands.

`Python 3.12` `FastAPI` `scikit-learn` `SQLite` `SQLAlchemy` `pytest`

---

### ⬡ [FleetPulse](https://sankartk.dev/projects/fleetpulse) · [Repo](https://github.com/Sankartk/fleetpulse)
Fleet maintenance REST API on Spring Boot + PostgreSQL — hourly scheduler catches overdue vehicles before anyone notices, idempotent alerting so the same event fires exactly once, role-based access control. **25+ endpoints, 16/16 integration tests green.**

`Java 21` `Spring Boot 3.2` `PostgreSQL` `Spring Data JPA` `Flyway` `Docker` `JUnit 5`

---

## Tech

**Languages** — Python, SQL, Java, TypeScript  
**Data & Databases** — PostgreSQL, Redshift, DynamoDB, Azure Synapse, SQLite, pandas, scikit-learn  
**Cloud & Infra** — AWS (ECS, EKS, Glue, Lambda, S3, Step Functions, Bedrock), Azure, Terraform, GitLab CI/CD, Docker  
**Frameworks** — Spring Boot 3, FastAPI, GraphQL, Next.js, Tailwind CSS  
**BI / Analytics** — Tableau, Power BI, Alteryx

---

## Certifications

AWS Solutions Architect – Associate · Alteryx Designer Core · Rising Star Award — Hexaware

---

📫 [LinkedIn](https://linkedin.com/in/sankartk11) · [Portfolio](https://sankartk.dev)
