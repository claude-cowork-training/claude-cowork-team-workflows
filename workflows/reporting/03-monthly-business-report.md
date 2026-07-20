# 03. Monthly Business Report

**Category:** Reporting · **Time saved:** ~2.5 hrs/month (estimate — based on replacing a half-day drafting session on the first business day of the month) · **Difficulty:** ●●○

**What it does:** Produces the one-page monthly business report from your metrics file, last month's report, and the owner's context notes — headline, numbers table with month-over-month deltas, drivers, and a mandatory risks section. Built to mirror how an operations lead actually writes it.

**You need:** A `monthly/` folder with `monthly-metrics.csv`, last month's report, and a `notes.md` where the report owner dumps context (the "why" behind the numbers).

## The prompt

```
Read monthly/monthly-metrics.csv, the most recent report in
monthly/reports/, and monthly/notes.md.
Write this month's report, one page, identical structure to last
month's:
- Headline first (the one sentence leadership should remember).
- The board numbers in a table with MoM deltas.
- "What drove it" — every surprising number gets a one-line cause,
  taken from notes.md; if notes.md doesn't explain it, write
  "needs explanation from [owner]".
- Risks & opportunities — this section is mandatory even in a good
  month.
Style per team-context/style-guide.md. Output as .docx, saved as
monthly/reports/monthly-report-YYYY-MM.docx.
```

## Setup (one time)

1. Create the folder; seed `reports/` with one real past report.
2. Put a recurring 15-minute calendar block on the owner's calendar for `notes.md` — the report is only as insightful as those notes.

## Running it (each time)

1. Confirm the metrics file has the new month's row; update notes.
2. Run, then read the risks section skeptically — Cowork drafts it, you own it.

## Adapt it

- **Weekly version:** that's workflow 01 — same skeleton, faster loop.
- **Investor update:** add "tone: external, no internal client names, no utilization detail".
- **Multi-entity:** one metrics file per business unit, plus a final consolidated page.

## Common failure + fix

**Failure:** Reporting a metric change without its cause — leadership always asks why, and a report that can't answer creates more work than it saves.
**Fix:** The "needs explanation from [owner]" instruction turns missing causes into a visible to-do list instead of a confident-sounding guess. In our Metamorfeus test (May 2026 data), the utilization spike was correctly flagged as a capacity risk only because the owner's notes said so — the CSV alone read it as a win.

---
→ Full guide: https://claudecoworktraining.com/guides/25-team-workflows/#03-monthly-business-report

→ Single-run prompt: [02. Draft a monthly business report from metrics, notes, and last month's example](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/documents-reports.md#02-draft-a-monthly-business-report-from-metrics-notes-and-last-months-example)
