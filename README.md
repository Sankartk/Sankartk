# Hi, I'm Sankar

I'm a software and data engineer in Newark, DE. For six years I've built the behind-the-scenes systems of finance: programs that move data between systems and check that it matches. The kind of thing nobody notices until it breaks.

My habits are simple. **Check data the moment it arrives. Make problems loud, not quiet. Put a person in the loop before anything that can't be undone.** Lately that has pulled me toward trading and AI: order books, strategy testing, and the checks that have to sit in front of AI-made decisions.

**[sankartk.dev](https://sankartk.dev)** has a short write-up for every project below.

---

## What I've been building

**[dlq-triage](https://github.com/Sankartk/dlq-triage)** · [write-up](https://sankartk.dev/projects/dlq-triage)
When messages fail and pile up in a queue, are they one problem or twelve? This groups them by cause (in my test run, 24 messages turned out to be 3 problems), then lets a person send one group back: practice run first, slow and stoppable, with a log of who did what. The AI explanation is optional and never sees customer data.
`Go` `GraphQL` `AWS SQS` `React` `TypeScript`

**[FinFlow](https://github.com/Sankartk/finflow)** · [write-up](https://sankartk.dev/projects/finflow)
The bank says a payment arrived on Aug 29; your books say Sep 1. Mistake or just timing? FinFlow compares two lists of payments and explains each mismatch, with simple checks first and a locally run AI model for the leftovers. Built and tested on generated transactions, not real bank data.
`Python` `Kafka` `PostgreSQL` `Ollama` `GraphQL`

**[regwatch](https://github.com/Sankartk/regwatch)** · [write-up](https://sankartk.dev/projects/regwatch)
An AI suggests a trade. Who checks it before money moves? A checkpoint with five rules, such as "never more than 10% in one stock" and "an AI-made trade needs a human's OK and a written reason". Every check is saved. It can also read new SEC filings and suggest rules for a person to approve.
`Python` `Ollama` `SQLite` `Streamlit`

**[alpha-engine](https://github.com/Sankartk/alpha-engine)** · [write-up](https://sankartk.dev/projects/alpha-engine)
Everyone has a trading strategy that "would have worked." This tries to prove it wouldn't: it never uses tomorrow's prices, charges trading costs, and tests on periods the strategy hasn't seen. Includes two simple strategies and a practice (paper) trading link to Alpaca.
`Python` `pandas` `Alpaca` `Streamlit`

**[market-microstructure](https://github.com/Sankartk/market-microstructure)** · [write-up](https://sankartk.dev/projects/market-microstructure)
What happens inside an exchange between "buy" and "filled"? A C++ program that rebuilds an order book from NASDAQ's real data format and flags four kinds of cheating. My first speed test said 45 ns per order; the honest number was 673 ns, and the README explains why.
`C++20` `CMake`

**[CashCast](https://github.com/Sankartk/cashcast)** · [write-up](https://sankartk.dev/projects/cashcast)
A branch orders next week's cash from gut feeling, plus 20% "just in case." This forecasts each branch's needs 14 days ahead and recommends an order amount. Built and tested on generated data for 6 branches, so its accuracy numbers describe the model, not a real bank.
`Python` `scikit-learn` `FastAPI`

**[Ops Copilot](https://github.com/Sankartk/ops-copilot-bedrock)** · [write-up](https://sankartk.dev/projects/ops-copilot)
2am, a service is down, and the fix is somewhere in a 40-page runbook. Ask in plain English and it finds the matching part of your runbooks and names the file it came from. A separate AWS workflow can roll back a bad deployment, but only after a person approves. A demo with three sample runbooks.
`Python` `Ollama` `AWS Lambda` `Step Functions`

**[FleetPulse](https://github.com/Sankartk/fleetpulse)** · [write-up](https://sankartk.dev/projects/fleetpulse)
A truck breaks down; its service was six weeks overdue. FleetPulse tracks vehicles, drivers and maintenance, and every hour raises one alert per overdue vehicle (not a duplicate every hour). 26 API endpoints and 16 tests.
`Java 21` `Spring Boot` `PostgreSQL` `Flyway`

---

## Tech

**Languages** — Go, Python, Java, C++, SQL, TypeScript
**Data** — PostgreSQL, Kafka, Redshift, DynamoDB, pandas, scikit-learn
**Cloud** — AWS (SQS, Glue, Lambda, Step Functions, Bedrock, ECS), Azure Synapse, Terraform, Docker
**Systems** — order books, strategy testing, message queues, compliance checks

---

[LinkedIn](https://linkedin.com/in/sankartk11) · [sankartk.dev](https://sankartk.dev) · karthicks399@gmail.com
