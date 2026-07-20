# 01. Weekly KPI Report

**Category:** Reporting · **Time saved:** ~2 hrs/week (estimate — based on replacing a manual pull-numbers-format-summarize routine that typically takes an afternoon block) · **Difficulty:** ●○○

**What it does:** Reads this week's metrics file and last week's report, produces a one-page KPI summary with week-over-week deltas and a one-line explanation for anything that moved more than 10%. Your Monday report writes itself; you review it instead of building it.

**You need:** A `kpi/` folder containing (a) a metrics CSV updated weekly, (b) last week's report as the format example, (c) your team-context folder (see [samples](../../templates/context-file-examples/)).

## The prompt

```
Read kpi/metrics.csv and the most recent report in kpi/reports/.
Produce this week's KPI report in exactly the same structure as the
most recent one:
- Headline first: the single most important change this week.
- A table of every metric with this week's value and the delta vs
  last week.
- One line of explanation for any metric that moved more than 10%.
  If the cause isn't in the data or my notes, write "cause unknown —
  needs input" instead of guessing.
Follow the style rules in team-context/style-guide.md.
Save as kpi/reports/kpi-report-YYYY-MM-DD.md using today's date.
If metrics.csv is missing this week's row, stop and tell me instead
of reusing last week's numbers.
```

## Setup (one time)

1. Create `kpi/` with a `reports/` subfolder; drop in one past report as the format anchor.
2. Agree who updates `metrics.csv` and by when (the workflow is only as fresh as that file).
3. Add your team-context folder next to it.

## Running it (each time)

1. Update `metrics.csv`, open Cowork on the folder, paste the prompt.
2. Review the "cause unknown" lines — those are the judgment calls the report exists for.
3. Send.

## Adapt it

- **Monthly cadence:** point it at monthly metrics and last month's report — this becomes workflow 03.
- **Per-client version:** one metrics file per client, run in a loop ("repeat for each subfolder in clients/").
- **Deck output:** change the last instruction to "produce a 3-slide summary deck (.pptx)".

## Common failure + fix

**Failure:** With no format example in `reports/`, Cowork invents its own structure — different every week, which defeats the purpose.
**Fix:** Always keep the most recent report in the folder; it's the de facto template. In our test with the Metamorfeus dataset, adding one example report eliminated structure drift entirely.

---
→ Full guide: https://claudecoworktraining.com/guides/25-team-workflows/#01-weekly-kpi-report

→ Single-run prompt: [01. Write a weekly KPI report from a metrics CSV and last week's report](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/documents-reports.md#01-write-a-weekly-kpi-report-from-a-metrics-csv-and-last-weeks-report)
