# 07. Notes → Action Items

**Category:** Meetings · **Time saved:** ~1 hr/week (estimate — based on replacing the manual after-meeting pass of extracting and assigning to-dos) · **Difficulty:** ●○○

**What it does:** Reads raw meeting notes — messy, abbreviated, half-sentences — and extracts a clean action-item list: task, owner, due date, and the source line it came from. Also flags decisions made and questions left open, so nothing dies in the notes file.

**You need:** A `notes/` folder where meeting notes land (any format), and a running `action-items.md` file.

## The prompt

```
Read the newest file in notes/.
Extract into three lists:
1. ACTION ITEMS — task, owner, due date. If the owner or date is
   not stated, write "UNASSIGNED" or "NO DATE" — do not infer them.
   Quote the source line under each item.
2. DECISIONS MADE — one line each.
3. OPEN QUESTIONS — anything raised but not resolved.
Then append the action items to action-items.md under today's
date, and flag any existing item in that file that these notes
show as completed.
```

## Setup (one time)

1. Create `notes/` and an empty `action-items.md`.
2. Agree the team convention: notes go in the folder same-day, however rough.

## Running it (each time)

1. Run after each meeting (or once daily across all new notes).
2. Fix the UNASSIGNED/NO DATE items in the next standup — the list makes the gaps visible.

## Adapt it

- **Project-tracker connector:** if Linear/Asana/etc. is connected, add "create the action items as tasks" instead of appending to a file.
- **Weekly sweep:** run across all of the week's notes at once — pairs with workflow 04.
- **Transcript input:** works on call transcripts too; add "ignore small talk and scheduling chatter".

## Common failure + fix

**Failure:** Cowork assigns owners by guessing from context ("Tomás reviewing extracts" → assigns every data task to Tomás), creating phantom commitments.
**Fix:** The hard "do not infer" rule plus the quoted source line — you can verify each extraction in two seconds. In our test on the Metamorfeus kickoff notes, the quoted-source rule caught one item that was actually a client's task, not ours.

---
→ Full guide: https://claudecoworktraining.com/guides/25-team-workflows/#07-notes-to-action-items

→ Single-run prompt: [43. Turn Raw Meeting Notes into an Action-Item Recap Email](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/email-communication.md#43-turn-raw-meeting-notes-into-an-action-item-recap-email)
→ Single-run prompt: [51. Turn Raw Meeting Notes into an Action Item Tracker](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/project-management.md#51-turn-raw-meeting-notes-into-an-action-item-tracker)
→ Single-run prompt: [52. Weekly Action Item Sweep Across All Meeting Notes](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/project-management.md#52-weekly-action-item-sweep-across-all-meeting-notes)
