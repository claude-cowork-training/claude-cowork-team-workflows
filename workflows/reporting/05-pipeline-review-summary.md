# 05. Pipeline Review Summary

**Category:** Reporting · **Time saved:** ~1 hr/week (estimate — based on replacing the manual prep for a weekly pipeline meeting) · **Difficulty:** ●○○

**What it does:** Turns a raw pipeline CSV into the meeting-ready view: total value by stage, leads that haven't been touched in 10+ days, and a recommended action per stale lead. The pipeline meeting starts at the decisions instead of at the spreadsheet.

**You need:** A `pipeline/` folder with your pipeline CSV (columns like: lead, source, stage, est_value, owner, last_touch).

## The prompt

```
Read pipeline/pipeline.csv. Today is [DATE].
Produce pipeline/pipeline-review-YYYY-MM-DD.md with:
1. Total pipeline value, and value by stage.
2. A "stale" table: every lead with last_touch more than 10 days
   ago — lead, owner, days since touch, est. value.
3. For each stale lead, one recommended action based on its stage
   and source (e.g., proposal sent + 2 weeks silent → "call, then
   mark cold if no response").
4. One line: biggest single risk to the pipeline number this week.
If any row has a missing owner or last_touch, list it under
"data problems" instead of skipping it silently.
```

## Setup (one time)

1. Export or maintain the pipeline CSV in the folder — column names can differ; just keep them consistent.
2. Adjust the staleness threshold (10 days) to your sales cycle.

## Running it (each time)

1. Refresh the CSV, set today's date in the prompt, run.
2. Bring the stale table to the meeting; the recommended actions are conversation starters, not verdicts.

## Adapt it

- **Recruiting pipeline:** candidates instead of leads — stages and staleness logic transfer directly.
- **CRM connector:** if your CRM is connected, replace the CSV read with a live pull; keep the same output format.
- **Owner-cut version:** add "group the stale table by owner" for 1:1 prep.

## Common failure + fix

**Failure:** Date-math mistakes when the CSV mixes date formats (2026-06-01 vs 06/01/2026), producing wrong staleness flags.
**Fix:** The "data problems" section catches malformed rows, and normalizing the export once fixes it permanently. Our test against the Metamorfeus pipeline (4 leads, one 3-weeks stale) flagged the right lead — Ozark Freight at 17 days — and recommended exactly the call-then-mark-cold action the team had independently decided on.

---
→ Full guide: https://claudecoworktraining.com/guides/25-team-workflows/#05-pipeline-review-summary

→ Single-run prompt: [13. Turn a Pipeline CSV into a Meeting-Ready Stale-Leads Summary](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/spreadsheets-data.md#13-turn-a-pipeline-csv-into-a-meeting-ready-stale-leads-summary)
