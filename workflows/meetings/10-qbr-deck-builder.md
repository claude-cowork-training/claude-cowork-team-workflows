# 10. QBR Deck Builder

**Category:** Meetings · **Time saved:** ~4 hrs/quarter per client (estimate — based on replacing the typical afternoon-plus of assembling a quarterly business review deck by hand) · **Difficulty:** ●●●

**What it does:** Builds the first full draft of a client QBR deck from the quarter's artifacts — engagement scope, status digests, metrics, and delivery notes — in your standard QBR structure: what we did, what it produced, what's next, and the renewal/expansion conversation starter.

**You need:** A per-client folder containing the engagement scope, the quarter's weekly digests or status notes, any metrics or outcome data, and one past QBR deck as the structure anchor.

## The prompt

```
Read everything in clients/[CLIENT]/ for this quarter, plus the
past QBR deck in clients/[CLIENT]/qbr/.
Build this quarter's QBR deck in the same structure:
1. Engagement summary — scope, term, owner.
2. What we delivered — from the digests and notes, concrete items
   only.
3. Outcomes — every figure must have a source file cited in the
   speaker notes; client-stated outcomes are labeled
   "client-reported, not independently measured".
4. What's next — open items and the coming quarter.
5. One renewal/expansion slide: the strongest evidence-based case
   for continuing, stated plainly.
Save as clients/[CLIENT]/qbr/qbr-YYYY-QN.pptx.
Anything you can't source gets "[NEEDS INPUT]", never a guess.
```

## Setup (one time)

1. Standardize the per-client folder so a quarter's story is in one place (workflows 04 and 07 feed it automatically).
2. Add your best past QBR deck as the anchor.

## Running it (each time)

1. Run two weeks before the QBR; the `[NEEDS INPUT]` flags become your prep list.
2. The renewal slide is a draft argument — the account owner rewrites it in their own voice.

## Adapt it

- **Internal quarterly review:** same skeleton pointed at a department folder.
- **One-pager companion:** add "also produce a one-page summary memo of the deck".
- **Multi-client batch:** loop over every client folder before renewal season.

## Common failure + fix

**Failure:** Outcome inflation — a client's casual "the digest saves us hours" becomes a hard ROI claim on a slide.
**Fix:** The sourcing rule and the "client-reported" label. Tested against the Metamorfeus Ferrostar engagement (alert volume reduced from ~1,400 to ~120/week, client-stated): the deck correctly carried the label — exactly the discipline you want in front of a client's leadership.

---
→ Full guide: https://claudecoworktraining.com/guides/25-team-workflows/#10-qbr-deck-builder

→ Single-run prompt: [22. Build a Client QBR Deck from the Quarter's Folder](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/presentations.md#22-build-a-client-qbr-deck-from-the-quarters-folder)
