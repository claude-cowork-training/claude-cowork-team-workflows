# 11. Campaign Performance Report

**Category:** Marketing · **Time saved:** ~2 hrs/week (estimate — based on replacing the Monday routine of pulling channel exports and rebuilding the same report) · **Difficulty:** ●●○

**What it does:** Reads your channel exports (ads, email, web analytics — as CSVs in one folder) and produces the weekly campaign report in your house format: spend, results, cost-per-result by channel, week-over-week deltas, and a plain-English "what to change" section.

**You need:** An `exports/` folder your team drops weekly channel CSVs into, last week's report as the format anchor, and your brand/team-context folder.

## The prompt

```
Read every CSV in campaigns/exports/ dated this week, and the most
recent report in campaigns/reports/.
Produce this week's report in the same structure:
1. Summary table: per channel — spend, primary result metric,
   cost per result, delta vs last week.
2. "What moved and why" — one line per >15% change; if the export
   doesn't show a cause, write "cause not in data".
3. "What to change" — max 3 recommendations, each tied to a number
   in the table.
Style per team-context/style-guide.md. Every number must trace to
an export file; note the source file per table row.
Save as campaigns/reports/campaign-report-YYYY-MM-DD.md.
If a channel's export is missing this week, list it as "no data
received" rather than repeating last week's figures.
```

## Setup (one time)

1. Standardize export drops: same folder, filename pattern like `channel-YYYY-MM-DD.csv`.
2. Seed `reports/` with one report you're proud of.

## Running it (each time)

1. Confirm all exports landed, run, review the 3 recommendations — accept, edit, or delete them; they're drafts.

## Adapt it

- **Monthly deep-dive:** point it at 4–5 weeks of exports, add "trend chart data per channel as a CSV".
- **Client-facing version:** add "external tone, no internal cost margins" for agency use.
- **Deck output:** swap the .md output for a 5-slide .pptx.

## Common failure + fix

**Failure:** Mixed metric names across platforms ("results" vs "conversions" vs "leads") get silently merged into one column, making channels incomparable.
**Fix:** Add a `metric-map.md` to the folder defining which export column is the "primary result" per channel — one file, permanent fix. This surfaced on our first synthetic-data test run and the map eliminated it.

---
→ Full guide: https://claudecoworktraining.com/guides/25-team-workflows/#11-campaign-performance-report

→ Single-run prompt: [15. Summarize Multi-Channel Campaign CSVs into One Performance Table](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/spreadsheets-data.md#15-summarize-multi-channel-campaign-csvs-into-one-performance-table)
