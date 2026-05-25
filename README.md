# JashwanthReddyE.github.io

Personal portfolio site for **Jashwanth Reddy Earla** — a senior data engineer building streaming lakehouses, dbt warehouses, and governed analytics platforms on **Azure** and **AWS**.

> Live: **[jashwanthreddye.github.io](https://jashwanthreddye.github.io)**

---

## About

Multi-cloud data engineer with **4+ years** shipping enterprise data platforms across **banking, retail, and healthcare**. I design the streaming layer, model the warehouse, wire up CI/CD, build the data-quality framework, and hand teams something they can operate without me on call. Lately I've been folding LLM-assisted tooling (Azure OpenAI, Claude, Copilot) into the development loop.

**Stack** — Azure · AWS · Snowflake · Databricks · dbt · Kafka · Event Hub · Terraform · Python · PySpark · SQL · Power BI

---

## What's in this repo

A single-page portfolio built as a hand-tuned `index.html` — no framework, no build step. Sections:

- **Hero** — typewriter intro, live pipeline visualization, headline stats
- **About** — background and approach
- **Experience** — tabbed timeline across CGI, Hexagon, Quality Theorem
- **Stack & Reference Architecture** — interactive terminal + tier diagram
- **Featured Projects** — deep-dives on shipped pipelines (below)
- **Contact** — email, LinkedIn, GitHub

Assets (architecture SVGs, dashboard screenshots) live under [`assets/`](assets/).

---

## Featured Projects

### Crypto Sentinel — AI Sentiment Pipeline
**[Live Dashboard](https://crypto-sentinel-dashboard.vercel.app/)** · **[Repo](https://github.com/JashwanthReddyE/crypto-sentinel)**

Azure Functions pipeline that scores 24 crypto assets daily and ranks them **BUY / WATCH / AVOID**. A timer-triggered function pulls live prices, market caps, and trending lists from CoinGecko plus headline sentiment from CryptoPanic. A 6-signal scoring engine (news sentiment + three momentum windows + volume ratio + trending bonus) collapses to a single 0–100 score, exposed through two HTTP endpoints and a self-contained Vercel dashboard. Runs at **~$0.03/month** on Consumption + LRS.

`Azure Functions v4` · `Python 3.11` · `CoinGecko` · `CryptoPanic` · `Vercel` · `pytest (144 tests)`

### Stock Sentiment & Forecast Pipeline
**[Repo](https://github.com/JashwanthReddyE/aws-stock-sentiment-pipeline)**

End-to-end AWS pipeline scoped to the Free Tier. EventBridge fires a Lambda every 30 min pulling Finnhub news; an S3 event triggers a second Lambda that scores headlines through **Bedrock Claude Haiku** and writes Parquet to silver. A daily forecast Lambda joins prices (Alpha Vantage) with sentiment via Athena, projects a 5-day trend, and asks Claude to write a plain-English market brief. Streamlit dashboard reads it back. All provisioned with Terraform.

`AWS Lambda` · `S3 Medallion` · `Bedrock` · `Glue + Athena` · `EventBridge` · `Streamlit` · `Terraform` · `pytest + moto`

---

## Other Repositories

| Repo | What it is |
| --- | --- |
| [crypto-sentinel](https://github.com/JashwanthReddyE/crypto-sentinel) | Azure Functions crypto sentiment + scoring pipeline (featured above) |
| [aws-stock-sentiment-pipeline](https://github.com/JashwanthReddyE/aws-stock-sentiment-pipeline) | AWS Lambda + Bedrock stock sentiment & forecast pipeline (featured above) |
| [sql-data-warehouse-project](https://github.com/JashwanthReddyE/sql-data-warehouse-project) | SQL Server data warehouse — ETL, dimensional modeling, analytics layer |
| [Gen-AI](https://github.com/JashwanthReddyE/Gen-AI) | Generative-AI experiments and notebooks (Python) |
| [IBM](https://github.com/JashwanthReddyE/IBM) | Coursework and labs from the IBM Data Science track (Jupyter) |
| [Portfolio](https://github.com/JashwanthReddyE/Portfolio) | Earlier portfolio iteration (HTML) |
| [double-pendulum](https://github.com/JashwanthReddyE/double-pendulum) | MATLAB simulation of a chaotic double-pendulum system |
| [INSE-6220](https://github.com/JashwanthReddyE/INSE-6220) | Concordia INSE 6220 — advanced statistical methods project |
| [INSE-6230](https://github.com/JashwanthReddyE/INSE-6230) | Concordia INSE 6230 — project data |
| [INSE-6210-Data](https://github.com/JashwanthReddyE/INSE-6210-Data) | Concordia INSE 6210 — final project dataset |
| [INSE-6250-Phonebook](https://github.com/JashwanthReddyE/INSE-6250-Phonebook) | Java phonebook app — software-quality coursework |
| [freecodecamp](https://github.com/JashwanthReddyE/freecodecamp) | freeCodeCamp exercises |

---

## Running locally

No build step. Clone and open `index.html` in a browser, or serve the directory:

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

Deployment is automatic via **GitHub Pages** from `main`.

---

## Contact

- **Email** — jashwanthreddyearla@gmail.com
- **GitHub** — [@JashwanthReddyE](https://github.com/JashwanthReddyE)
- **Site** — [jashwanthreddye.github.io](https://jashwanthreddye.github.io)
