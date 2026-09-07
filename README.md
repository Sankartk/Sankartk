# Hi, I'm Sankar

I'm a software and data engineer in Newark, DE. Six years building pipelines and backend systems in finance — the parts nobody notices until they break.

The through-line in everything I build: **systems that don't trust their own input.** Pipelines that validate before they propagate. Automation that pauses before it does something permanent. Lately that's pulled me toward trading and AI — order books, backtesting, and the compliance layer that has to sit in front of AI-generated decisions.

**[sankartk.dev](https://sankartk.dev)** — every project below has a full write-up there.

---

## What I've been building

**[regwatch](https://github.com/Sankartk/regwatch)** · [write-up](https://sankartk.dev/projects/regwatch)
A compliance gate for AI-generated trades. Five rules — position limits, restricted lists, wash trades, concentration, and an AI governance rule enforcing EU AI Act Article 14 (human approval + explainable rationale, or the trade doesn't execute). Pulls fresh SEC filings and has a local LLM draft candidate rules for human review. Every check lands in an immutable audit trail.
`Python` `Ollama` `SEC EDGAR` `SQLite` `Streamlit`

**[market-microstructure](https://github.com/Sankartk/market-microstructure)** · [write-up](https://sankartk.dev/projects/market-microstructure)
A limit order book in C++20 that reads NASDAQ's actual wire format (ITCH 5.0) and detects spoofing, layering, momentum ignition, and quote stuffing in-process. Pool allocator, fixed-point prices, zero allocations after warmup. Measured: 673ns add / 29ns cancel — the README explains why my first numbers were wrong, which taught me more than the code did.
`C++20` `CMake` `ITCH 5.0` `ctest`

**[alpha-engine](https://github.com/Sankartk/alpha-engine)** · [write-up](https://sankartk.dev/projects/alpha-engine)
A backtester built to prove you wrong. Weights are shifted a day before touching returns (lookahead is structurally impossible), every rebalance pays spread + square-root market impact, and walk-forward validation exposes overfit strategies. Ships with momentum and mean-reversion strategies and a live paper-trading loop against Alpaca.
`Python` `pandas` `Alpaca` `Streamlit` `pytest`

**[FinFlow](https://github.com/Sankartk/finflow)** · [write-up](https://sankartk.dev/projects/finflow)
AI-native reconciliation engine. Kafka ingestion with checkpoint replay, a five-pass matching pipeline (exact → timing → fuzzy reference → amount → LLM), and pgvector so the system remembers past anomalies. 94%+ auto-match rate, zero external API costs.
`Python` `Kafka` `PostgreSQL` `pgvector` `Ollama` `GraphQL`

**[CashCast](https://github.com/Sankartk/cashcast)** · [write-up](https://sankartk.dev/projects/cashcast)
Branch vault cash forecasting. Ridge regression per branch over 730 days, Isolation Forest for anomalies, 14-day horizon with confidence bands — avg MAPE 9.1%. Turns the standard 15–20% "buffer guess" into a number with a reason behind it.
`Python` `scikit-learn` `FastAPI` `Plotly`

**[Ops Copilot](https://github.com/Sankartk/ops-copilot-bedrock)** · [write-up](https://sankartk.dev/projects/ops-copilot)
RAG over your own runbooks for 2am incidents. Answers cite the exact file and line, and remediation pauses at an SNS approval gate — nothing touches production until a human says so. One env var switches between Ollama local and AWS Bedrock.
`Python` `FAISS` `AWS Bedrock` `Step Functions` `SAM`

**[FleetPulse](https://github.com/Sankartk/fleetpulse)** · [write-up](https://sankartk.dev/projects/fleetpulse)
Fleet maintenance ops on Spring Boot + PostgreSQL. Hourly scheduler catches overdue vehicles, alerts are idempotent, 25+ endpoints, 16/16 integration tests green.
`Java 21` `Spring Boot` `PostgreSQL` `Flyway` `Docker`

---

## Tech

**Languages** — Python, Java, C++, SQL, TypeScript
**Data** — PostgreSQL, Kafka, Redshift, DynamoDB, pgvector, pandas, scikit-learn
**Cloud** — AWS (Glue, Lambda, Step Functions, Bedrock, ECS), Azure Synapse, Terraform, Docker
**Systems** — order books, backtesting engines, binary protocols, compliance pipelines

---

[LinkedIn](https://linkedin.com/in/sankartk11) · [sankartk.dev](https://sankartk.dev) · karthicks399@gmail.com
