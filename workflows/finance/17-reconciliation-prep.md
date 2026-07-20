# 17. Reconciliation Prep

**Category:** Finance · **Time saved:** ~2 hrs/month (estimate — based on replacing the manual line-matching phase; exception judgment remains human) · **Difficulty:** ●●○

**What it does:** Matches line items across two exports — bank vs ledger, invoices vs payments, system A vs system B — and produces a clean exception report: matched (with match basis), unmatched on each side, and near-matches needing a human eye. Your analysts start at the interesting part.

**You need:** A `recon/` folder with the two files to match and a `match-rules.md` (what counts as a match: exact amount + date window? reference number?).

## The prompt

```
Read recon/file-a.csv, recon/file-b.csv, and recon/match-rules.md.
Match line items per the rules and produce
recon/exceptions-YYYY-MM.md:
1. MATCHED — count and total value only (no need to list them).
2. NEAR MATCHES — pairs that match on some rules but not all
   (e.g., amount matches, date outside window), shown side by side
   with what differs.
3. UNMATCHED IN A / UNMATCHED IN B — full rows.
4. DATA PROBLEMS — malformed rows, duplicate references,
   inconsistent date formats.
Apply the rules mechanically — do not decide that a near match
"probably" matches. Every judgment stays in the NEAR MATCHES list.
```

## Setup (one time)

1. Write `match-rules.md` — 15 minutes with whoever does this manually today; their heuristics ARE the rules.
2. Test once on a prior month where you know the answer.

## Running it (each time)

1. Drop the two exports, run, work the near-match and unmatched lists.
2. Rules evolve: when a near-match pattern repeats monthly, add it to `match-rules.md` as an explicit rule.

## Adapt it

- **Invoice vs payment:** match your invoice register against payment confirmations — pairs with workflow 19.
- **Expense vs card feed:** submitted expenses against the card statement.
- **Three-way:** PO vs invoice vs receipt; add a third file and extend the rules.

## Common failure + fix

**Failure:** Date-format chaos (2026-04-07 vs 04/07/2026 vs "Apr 15 2026" in one file) silently breaks the date-window rule.
**Fix:** The DATA PROBLEMS section catches it; add "normalize all dates to YYYY-MM-DD before matching" once you've seen your exports' habits. Our test data (the Metamorfeus April expenses file) deliberately mixes three date formats — the workflow flags all three styles on the first run.

---
→ Full guide: https://claudecoworktraining.com/guides/25-team-workflows/#17-reconciliation-prep

→ Single-run prompt: [11. Match Two Exports and Produce an Exception Report](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/spreadsheets-data.md#11-match-two-exports-and-produce-an-exception-report)
