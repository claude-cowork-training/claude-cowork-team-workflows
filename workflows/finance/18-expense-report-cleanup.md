# 18. Expense Report Cleanup

**Category:** Finance · **Time saved:** ~1 hr/month (estimate — based on replacing the manual tidy-and-chase pass before expenses go to accounting) · **Difficulty:** ●○○

**What it does:** Takes the team's raw expense submissions — inconsistent dates, missing notes, uncategorized rows — and produces a standardized expense file plus a per-person chase list of what's missing (receipts, notes, categories). The monthly nag writes itself.

**You need:** An `expenses/` folder with the month's raw CSV(s) and a `categories.md` listing valid categories and what requires a receipt or note.

## The prompt

```
Read expenses/expenses-YYYY-MM.csv and expenses/categories.md.
Produce two outputs:
1. expenses/clean/expenses-YYYY-MM-clean.csv — dates normalized to
   YYYY-MM-DD, categories mapped to the valid list, amounts as
   plain numbers, sorted by person then date. Never delete or
   merge rows; anything unfixable goes through unchanged and gets
   flagged.
2. expenses/chase-list-YYYY-MM.md — grouped by person: missing
   notes, missing receipts per the rules, uncategorizable items,
   and totals per person.
Do not infer categories from vague notes — flag them instead.
```

## Setup (one time)

1. Write `categories.md` with your valid categories and receipt rules.
2. Agree the submission cutoff so one run covers the month.

## Running it (each time)

1. Run after the cutoff; forward each person their chase-list section.
2. The clean CSV goes to accounting only after the chase items resolve.

## Adapt it

- **Weekly cadence:** smaller chase lists, less month-end pile-up.
- **Per-client billing tags:** add a rule mapping expenses to client codes for rebilling.
- **Policy checks:** add limits ("flag meals over $75") to `categories.md` — the chase list becomes a soft policy gate.

## Common failure + fix

**Failure:** Overconfident category inference — "data tool subscription" auto-filed under Software is fine; "client dinner" silently split from Travel is not, and miscategorized rows are invisible downstream.
**Fix:** The flag-don't-infer rule for anything ambiguous. Tested on the Metamorfeus April expenses (mixed date formats, one row missing a note): all three date styles normalized correctly and the missing note surfaced on the right person's chase list.

---
→ Full guide: https://claudecoworktraining.com/guides/25-team-workflows/#18-expense-report-cleanup

→ Single-run prompt: [12. Clean a Raw Expense CSV and Build a Missing-Items Chase List](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/spreadsheets-data.md#12-clean-a-raw-expense-csv-and-build-a-missing-items-chase-list)
