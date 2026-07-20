# 19. Invoice Tracker & Chase List

**Category:** Finance · **Time saved:** ~1.5 hrs/month (estimate — based on replacing the manual scan of sent invoices against payments and drafting reminder notes) · **Difficulty:** ●○○

**What it does:** Reads your invoices folder and payment notes and produces the receivables picture: every outstanding invoice with days outstanding, an aging summary, and a drafted (never sent) chase note per overdue invoice matched to how overdue it is — friendly at day 5, firm at day 45.

**You need:** An `invoices/` folder (the invoice files themselves, any naming), a `payments.md` or CSV noting what's been paid, and your style guide.

## The prompt

```
Read every invoice in invoices/sent/ and invoices/payments.md.
Today is [DATE]. Produce invoices/receivables-YYYY-MM-DD.md:
1. Outstanding invoices table: number, client, amount, issue date,
   terms, days outstanding, status (current / overdue).
2. Aging summary: current, 1–30, 31–60, 60+.
3. For each overdue invoice, a drafted chase note in our style —
   tone scaled to lateness (gentle reminder ≤14 days overdue;
   direct with a requested payment date beyond that). Save drafts
   to invoices/chase-drafts/, do not send anything.
If an invoice's terms or issue date can't be read from the file,
list it under "unreadable — check manually" rather than assuming
net 30.
```

## Setup (one time)

1. Keep sent invoices in one folder; log payments in one place as they land.
2. Add one past chase email you liked to teach the tone.

## Running it (each time)

1. Run weekly or with the monthly close; review drafts before sending — you know which client has a payment run on the 25th.

## Adapt it

- **Accounting-system export:** replace folder-reading with your AR export; keep the chase-draft logic.
- **Payables mirror:** flip it — what WE owe, sorted by due date.
- **Cash forecast:** add "project expected receipts per week assuming historical payment behavior — labeled as an estimate".

## Common failure + fix

**Failure:** Inconsistent invoice formats (some structured, some three scrappy lines) make Cowork guess missing terms — and a guessed due date produces a wrongly-timed chase.
**Fix:** The "unreadable — check manually" rule. Tested on the Metamorfeus invoice set (one formal invoice, one informal note-style file with a question mark in it): the formal one tracked cleanly, the scrappy one was correctly flagged for a human instead of chased on invented terms.

---
→ Full guide: https://claudecoworktraining.com/guides/25-team-workflows/#19-invoice-tracker-chase-list

→ Single-run prompt: [14. Build an Invoice Aging Table from a Folder of Invoices](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/spreadsheets-data.md#14-build-an-invoice-aging-table-from-a-folder-of-invoices)
