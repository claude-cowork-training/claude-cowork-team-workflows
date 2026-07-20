# 04. Weekly Client Status Digest

**Category:** Reporting · **Time saved:** ~1.5 hrs/week (estimate — based on replacing a Friday-afternoon routine of rereading the week's notes and assembling statuses by hand) · **Difficulty:** ●○○

**What it does:** Reads the week's meeting notes and your pipeline file, and produces a one-page digest: one section per active client with a green/yellow/red status, a one-line reason, and a named next action with an owner. Ends with a "needs a decision" list.

**You need:** A `digest/` folder with `weekly-inputs/` (this week's meeting notes + pipeline CSV), one example of a good past digest, and your team-context folder.

## The prompt

```
Read everything in digest/weekly-inputs/ and the example in
digest/examples/.
Write this week's client status digest in exactly the example's
format: one section per active client, max 5 lines each, with
status (GREEN/YELLOW/RED), a one-line why, and next action +
owner + date.
A RED status must include a named recovery action.
End with a "Needs a decision" list — include it even if empty.
Statuses come from evidence in the notes, not optimism: if the
notes don't support GREEN, it isn't GREEN.
Save as digest/client-digest-YYYY-MM-DD.md.
```

## Setup (one time)

1. Create the folders; write (or borrow) one example digest — that file defines "good" more powerfully than any instruction.
2. Make dropping meeting notes into `weekly-inputs/` a team habit; the digest is a mirror of what's in that folder.

## Running it (each time)

1. Friday 15:00: confirm the week's notes are in, run the prompt.
2. Sanity-check the statuses against your gut — disagreement usually means a note is missing, which is itself useful signal.

## Adapt it

- **Internal projects instead of clients:** one section per project; statuses work identically.
- **Slack-length version:** add "then produce a 5-line Slack summary of the digest".
- **Monthly roll-up:** point it at four weeks of digests and ask for trend lines per client.

## Common failure + fix

**Failure:** Status inflation — everything comes back GREEN because the notes are sparse and Cowork fills the vacuum charitably.
**Fix:** The "evidence, not optimism" line plus the example file. In testing with the Metamorfeus week (extract quality issue at one client), the digest correctly held that client at YELLOW only after we added the evidence rule; before it, the same inputs produced GREEN.

---
→ Full guide: https://claudecoworktraining.com/guides/25-team-workflows/#04-weekly-client-status-digest

→ Single-run prompt: [03. Build a weekly client status digest from a folder of meeting notes](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/documents-reports.md#03-build-a-weekly-client-status-digest-from-a-folder-of-meeting-notes)
