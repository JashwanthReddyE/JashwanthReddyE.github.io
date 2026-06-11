# Jashwanth Reddy Earla — Portfolio

A single-file, zero-dependency portfolio site (`index.html`) themed as a **living data platform**. No build step, no framework — just open it or host it anywhere static.

## Dynamic features

- **Terminal boot sequence** on first visit (`$ jash --wake portfolio`), skippable, once per session
- **Interactive SQL console** — visitors can actually query the portfolio (`SHOW TABLES`, `SELECT … WHERE … ILIKE`, `ORDER BY`, `LIMIT`, `count(*)`, `DESCRIBE`, `EXPLAIN`, ↑ history, `sudo hire me`); press `/` to jump to it
- **Airflow-style DAG nav** in the hero — tasks flip queued → running → done as you scroll; click to jump
- **Animated recruiter-facing stat counters** — years, industries, batch-runtime cuts, engineers mentored
- **Streaming event-log bar** (bottom) — pipeline events with a running ingest counter
- **Mouse-reactive medallion canvas** — particles flow bronze → silver → gold, deflect around the cursor; click to drop a record
- UTC clock, scroll-progress bar, scroll-spy, typewriter, radar/story/signal project visuals
- All animation respects `prefers-reduced-motion`

## Preview locally

```powershell
python -m http.server 4173
# open http://localhost:4173
```

## Deploy

- **GitHub Pages** — copy `index.html` into the `JashwanthReddyE.github.io` repo and push; it goes live at https://jashwanthreddye.github.io/ (the URL the resume already links to).
- **Vercel** — `vercel --prod` from this folder.

## Editing content

Everything lives in `index.html`:

| What | Where |
|---|---|
| Hero headline, typewriter phrases, stats | `<header>` + the `phrases` array in the script |
| SQL console data (tables/rows) | the `DB` object in the `sqlConsole` IIFE |
| Boot log lines | the `lines` array in the `boot` IIFE |
| Event-log messages | the `pool` array in the `evlog` IIFE |
| Skills chips | `#skills` section |
| Experience bullets + run-status strips | `#experience` section (`.job` articles) |
| Project cards, lineage rows, links | `#projects` section (`.proj-card` articles) |
| Contact links | `#contact` section |

Highlighted metrics use `<span class="m">…</span>`; tech tags use `<span class="chip">…</span>`.
