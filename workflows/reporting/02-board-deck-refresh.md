# 02. Board Deck Refresh

**Category:** Reporting · **Time saved:** ~3 hrs/month (estimate — based on replacing the evening of copy-paste that deck refreshes usually consume) · **Difficulty:** ●●○

**What it does:** Takes last period's board/leadership deck and this period's numbers and produces an updated deck with the same structure, refreshed figures, and flagged talking points — instead of you rebuilding slides by hand and hunting for every stale number.

**You need:** A `board/` folder with last period's deck (.pptx), the current metrics file, and a short notes file with anything leadership must hear this period.

## The prompt

```
Read the most recent deck in board/, board/metrics.csv, and
board/notes.md.
Create this period's deck: identical slide structure and order,
every figure updated from metrics.csv, and the points in notes.md
worked into the relevant slides as speaker notes.
Flag any slide where the new numbers change the story (e.g., a
trend reverses) by adding "[REVIEW]" to its title.
Do not add, remove, or redesign slides.
Save as board/board-deck-YYYY-MM.pptx.
If any figure in the old deck has no matching source in
metrics.csv, mark it "[SOURCE?]" rather than carrying it forward.
```

## Setup (one time)

1. Create `board/`; add the last approved deck and the metrics file.
2. Start the habit: 10 minutes before running it, jot leadership context into `notes.md` (this is where the value concentrates).

## Running it (each time)

1. Update metrics and notes, run the prompt.
2. Search the output for `[REVIEW]` and `[SOURCE?]` — those are your actual work.
3. Present.

## Adapt it

- **Quarterly:** same prompt, quarterly metrics — pairs with workflow 10 (QBR builder) for client-facing versions.
- **Exec one-pager instead:** replace the deck instruction with "a one-page memo in the structure of memo-example.md".
- **Department roll-up:** point it at multiple team folders and add "one summary slide per department".

## Common failure + fix

**Failure:** Old decks contain hand-typed numbers with no source, and Cowork silently carries them forward — stale figures in front of the board.
**Fix:** The `[SOURCE?]` instruction above exists because of this. In testing against the Metamorfeus Q1 files, two orphan figures surfaced on the first run; fix the source file once and they stay fixed.

---
→ Full guide: https://claudecoworktraining.com/guides/25-team-workflows/#02-board-deck-refresh

→ Single-run prompt: [21. Refresh Last Period's Board Deck with This Period's Numbers](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/presentations.md#21-refresh-last-periods-board-deck-with-this-periods-numbers)
→ Single-run prompt: [24. Audit a Deck for Numbers with No Source File](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/presentations.md#24-audit-a-deck-for-numbers-with-no-source-file)
