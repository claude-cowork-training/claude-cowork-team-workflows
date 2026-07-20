# 09. Follow-Up Email Drafter

**Category:** Meetings · **Time saved:** ~1.5 hrs/week (estimate — based on replacing 15–20 minutes of drafting per external meeting) · **Difficulty:** ●○○

**What it does:** Turns meeting notes into a ready-to-review follow-up email in your team's voice: thanks, what was agreed, who owes what by when, and the next step. Drafts, never sends — you stay the sender.

**You need:** A `notes/` folder, your team-context folder (the style guide matters most here), and optionally one example of a follow-up email you were happy with.

## The prompt

```
Read the newest file in notes/ and team-context/style-guide.md
(and the example in examples/follow-up-example.md if present).
Draft a follow-up email to the external attendees:
- One line of thanks, no flattery.
- "What we agreed" — bullet list, each with an owner and date.
- "Next step" — a single, specific line.
- Anything the notes mark as sensitive or internal-only must NOT
  appear in the draft.
Match the example's tone. Keep it under 150 words.
Save as drafts/follow-up-YYYY-MM-DD-[client].md. Do not send
anything — draft only.
```

## Setup (one time)

1. Add one good past follow-up as `examples/follow-up-example.md` — tone is learned from examples, not adjectives.
2. Mark internal-only content in your notes with a convention like `[INTERNAL]`.

## Running it (each time)

1. Run within an hour of the meeting while you can still catch errors.
2. Read the "what we agreed" bullets against your memory — this is the one section that must be exactly right.

## Adapt it

- **Email connector:** if connected, change to "create as a draft in my email" — still never auto-send.
- **Two-audience version:** one external follow-up + one internal debrief with the `[INTERNAL]` content included.
- **Proposal follow-up:** add "reference the open proposal and its stated timeline".

## Common failure + fix

**Failure:** Internal detail leaking into an external draft — pricing margins, candid client assessments — because the notes mix both.
**Fix:** The `[INTERNAL]` marker convention plus the explicit exclusion rule. Tested against Metamorfeus notes containing an internal budget-signal remark: with the rule, the draft cleanly omitted it; without, it paraphrased it straight to the client.

---
→ Full guide: https://claudecoworktraining.com/guides/25-team-workflows/#09-follow-up-email-drafter

→ Single-run prompt: [41. Draft a Client Follow-Up Email from Meeting Notes](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/email-communication.md#41-draft-a-client-follow-up-email-from-meeting-notes)
→ Single-run prompt: [42. Write One External Follow-Up and One Internal Debrief from the Same Notes](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/email-communication.md#42-write-one-external-follow-up-and-one-internal-debrief-from-the-same-notes)
