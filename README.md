# JashwanthReddyE.github.io

Source for my **Data Engineer portfolio site** — live at **[jashwanthreddye.github.io](https://jashwanthreddye.github.io)**.

A single-page, dark-themed portfolio designed around the idea that *compliance, engineers, and executives should all be able to trust the same platform*. It walks through where I've shipped, the architecture pattern I keep coming back to (Lambda-style real-time + batch on Azure / AWS), specific wins with numbers, and a featured-project deep dive on my **Stock Sentiment & Forecast Pipeline**.

---

## Sections

| § | Section | What it covers |
|---|---|---|
| 01 | **Intro** | Senior Data Engineer · 4+ years · Azure + AWS · banking, retail, healthcare. |
| 02 | **Experience** | Sr. Data Engineer @ CGI · Data Engineer @ Hexagon · Data Engineer @ Quality Theorem. |
| 03 | **Reference Architecture** | The Lambda-style streaming + batch pattern I default to — Event Hub / Kafka → Databricks Structured Streaming → medallion lakehouse → Snowflake / Synapse / Redshift. |
| 04 | **Toolkit** | Filterable, terminal-style command palette of the stack I work in. |
| 05 | **Wins with numbers** | T+1 batch → sub-8-second event-to-alert · 8h → 2h monthly close · NL → SQL assistant for risk analysts · new-source onboarding 3 weeks → 4 days · dashboard p95 25s → <5s · audit-ready PHI lineage. |
| 06 | **Featured Projects** | [`AISLakehouse`](https://github.com/JashwanthReddyE/AISLakehouse) — real-time maritime medallion lakehouse (AISStream → Event Hubs → Databricks + ADLS Gen2 → dark-vessel analytics, [live](https://aislakehouse.vercel.app)) · [`crypto-sentinel`](https://github.com/JashwanthReddyE/crypto-sentinel) — Azure Functions AI sentiment pipeline ([live](https://crypto-sentinel-dashboard.vercel.app)) · [`aws-stock-sentiment-pipeline`](https://github.com/JashwanthReddyE/aws-stock-sentiment-pipeline) — AWS Lambda + Bedrock + Streamlit. Each with architecture diagram and design decisions. |
| 07 | **Contact** | LinkedIn · email. |

---

## Stack

- **HTML5** — single semantic `index.html`, one-file site
- **CSS3** — design tokens via CSS custom properties, mobile-first responsive layout, schema-grid backdrop, cursor glow
- **JavaScript** — vanilla, no framework — scroll reveal, command-palette toggle, architecture accordion (mobile)
- **Fonts** — Fraunces (display), Inter Tight (body), JetBrains Mono (code)
- **Hosted on** — GitHub Pages

No build step. No bundler. No dependencies. Just open the HTML.

---

## Repo layout

```
JashwanthReddyE.github.io/
├── index.html                              # Entire site — markup + CSS + JS inline
└── assets/
    ├── stock-sentiment-architecture.png    # AWS pipeline architecture diagram
    ├── stock-sentiment-brief.png           # Dashboard — AI Forecast & Brief tab
    ├── stock-sentiment-heatmap.png         # Dashboard — Sentiment Heatmap tab
    └── stock-sentiment-prices.png          # Dashboard — Live Prices tab
```

---

## Run locally

```bash
git clone https://github.com/JashwanthReddyE/JashwanthReddyE.github.io.git
cd JashwanthReddyE.github.io
python -m http.server 8000
# Visit http://localhost:8000
```

---

## Deploy

Pushes to `main` are served automatically by GitHub Pages at **[jashwanthreddye.github.io](https://jashwanthreddye.github.io)**.

---

*Author — [Jashwanth Reddy Earla](https://github.com/JashwanthReddyE) · Senior Data Engineer · Montreal, Canada · [LinkedIn](https://www.linkedin.com/in/jashwanthreddye/)*
