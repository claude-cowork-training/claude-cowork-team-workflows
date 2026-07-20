# 20. Variance Commentary Draft

**Category:** Finance · **Time saved:** ~2 hrs/month (estimate — based on replacing the first-draft phase of monthly variance commentary; the judgment calls stay with finance) · **Difficulty:** ●●○

**What it does:** Compares actuals to budget (or prior period) from your spreadsheets and drafts the variance commentary in your house format: variance table, a draft explanation per material variance from the context notes, and explicit "[JUDGMENT]" flags where the explanation genuinely requires a finance brain.

**You need:** A `variance/` folder with actuals and budget files, a materiality threshold in the prompt, a `context-notes.md`, and last month's commentary as the format anchor.

## The prompt

```
Read variance/actuals-YYYY-MM.csv, variance/budget-YYYY.csv,
variance/context-notes.md, and last month's commentary in
variance/reports/.
Materiality: variances over 10% AND over $2,000.
Produce this month's commentary in the same format:
1. Variance table: line item, actual, budget, variance $ and %,
   material yes/no.
2. For each material variance, a one-paragraph draft explanation —
   ONLY from context-notes.md or clear patterns in the data
   (timing shift visible across months). Anything else gets
   "[JUDGMENT: likely candidates are X or Y — finance to
   confirm]".
Never write a confident explanation you cannot source. Label any
forward-looking statement as an expectation, not a fact.
Save as variance/reports/variance-YYYY-MM.md.
```

## Setup (one time)

1. Align file structures once (same line-item names in actuals and budget — or add a mapping file).
2. Set your real materiality threshold in the prompt.

## Running it (each time)

1. Run after the close (workflow 16 feeds it); finance resolves the `[JUDGMENT]` flags — that's the actual work, now isolated and visible.

## Adapt it

- **Quarterly board version:** roll three months up, external tone.
- **Department cut:** variance by cost center with an owner column.
- **Forecast vs actual:** swap budget for the latest forecast to test forecasting quality.

## Common failure + fix

**Failure:** Plausible-sounding causal stories for variances ("increased headcount drove the rise") that no source supports — the classic way an AI draft erodes trust with a CFO.
**Fix:** The source-or-flag rule. In our synthetic-data test, an unexplained revenue jump came back as a `[JUDGMENT]` flag with two candidate causes rather than a confident invention — and the context-notes explanation (a first milestone payment) was used verbatim where it existed.

---
→ Full guide: https://claudecoworktraining.com/guides/25-team-workflows/#20-variance-commentary-draft

→ Single-run prompt: [05. Draft variance commentary comparing actuals to budget spreadsheets](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/documents-reports.md#05-draft-variance-commentary-comparing-actuals-to-budget-spreadsheets)
