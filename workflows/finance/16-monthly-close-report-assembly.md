# 16. Monthly Close Report Assembly

**Category:** Finance · **Time saved:** ~3 hrs/month (estimate — based on replacing the assembly-and-formatting portion of a close package; the accounting judgment stays with your team) · **Difficulty:** ●●○

**What it does:** Collects the month's close outputs from a folder — trial balance export, revenue detail, notes from the controller — and assembles the standard monthly close report in your house structure, with every figure traced to a source file and every anomaly flagged rather than smoothed over.

**You need:** A `close/YYYY-MM/` folder your team drops exports into, last month's close report as the format anchor, and a `close-notes.md` for context.

## The prompt

```
Read every file in this month's close folder (close/YYYY-MM/ —
use the current month) and last month's report in close/reports/.
Assemble this month's close report in the identical structure:
1. Summary figures with MoM deltas, each traced to its source
   export (cite file + row/section).
2. Notable items — anything >10% off prior month or budget, with
   the explanation from close-notes.md; if the notes don't explain
   it, flag "[EXPLAIN: ...]" for the controller.
3. Open items — anything the exports show as unreconciled or
   pending.
Never net, adjust, or reclassify figures — report them exactly as
exported and flag inconsistencies instead.
Output as .docx: close/reports/close-report-YYYY-MM.docx (same
month as the folder).
If an expected export is missing, stop and list what's missing.
```

## Setup (one time)

1. Standardize the drop folder and export set (same reports from your system every month).
2. Give the controller a 10-minute `close-notes.md` habit — the flags shrink every month it exists.

## Running it (each time)

1. Run once all exports land; work the `[EXPLAIN]` flags; controller signs off.
2. The report is a draft for review, never a final record on its own.

## Adapt it

- **Weekly flash version:** a 5-line summary from just the revenue export, every Friday.
- **Board pack feed:** the output becomes an input to workflow 02.
- **Multi-entity:** one folder per entity plus a consolidation section (add "do not eliminate intercompany — flag it").

## Common failure + fix

**Failure:** Helpful "corrections" — Cowork reconciling a discrepancy between two exports by picking one, when the discrepancy IS the finding.
**Fix:** The never-adjust rule. In testing with intentionally inconsistent synthetic exports, the rule converted a silent pick into a flagged discrepancy — which is the whole job.

---
→ Full guide: https://claudecoworktraining.com/guides/25-team-workflows/#16-monthly-close-report-assembly

→ Single-run prompt: [04. Assemble a monthly close report from a folder of finance exports](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/documents-reports.md#04-assemble-a-monthly-close-report-from-a-folder-of-finance-exports)
