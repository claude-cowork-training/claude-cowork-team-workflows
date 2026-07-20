# 06. Meeting Prep Pack

**Category:** Meetings · **Time saved:** ~2 hrs/week (estimate — based on replacing 15–20 minutes of scrambling before each of a week's external meetings) · **Difficulty:** ●●○

**What it does:** Looks at tomorrow's calendar, pulls the relevant history for each meeting from your notes and client folders, and produces a one-paragraph briefing per meeting: who, what happened last, open items, and the one thing not to forget. You walk in prepared without the 8:45am archaeology.

**You need:** A calendar connector (or an exported calendar file as fallback), a `clients/` or `notes/` folder Cowork can read, and your team-context folder.

## The prompt

```
Look at tomorrow's calendar. For each meeting that involves someone
outside our team:
1. Identify the client or topic.
2. Search clients/ and notes/ for the most recent notes, open
   action items, and any unresolved issues involving them.
3. Write a briefing of max one paragraph: attendees, where things
   stand, open items with owners, and one "don't forget" line.
Order the briefings by meeting time. Skip internal 1:1s and
standups unless an open action item mentions them.
Save as prep/meeting-prep-YYYY-MM-DD.md.
If you can't find any history for a meeting, say "no prior
context found" — don't invent background.
```

## Setup (one time)

1. Connect your calendar (or set up a weekly calendar export into the folder).
2. Make sure meeting notes actually land in `notes/` — this workflow surfaces whatever note-taking discipline you have.

## Running it (each time)

1. Run at end of day; read the pack with coffee the next morning.
2. The "don't forget" lines are Cowork's inference — verify the ones that matter.

## Adapt it

- **Weekly version:** "the coming week" instead of tomorrow, grouped by day.
- **Exec version:** one combined page for a leader's whole day, 3 lines per meeting max.
- **Pre-sales version:** add "for pipeline leads, include stage and last touch from pipeline.csv".

## Common failure + fix

**Failure:** Without the "no prior context found" rule, Cowork writes plausible-sounding background for meetings it has no data on — which is worse than no briefing.
**Fix:** That rule, plus keeping notes in predictable folders. Tested against the Metamorfeus simulated calendar (5 meetings incl. a new-lead intro call): the intro call correctly came back as "no prior context found" except its webinar signup source.

---
→ Full guide: https://claudecoworktraining.com/guides/25-team-workflows/#06-meeting-prep-pack

→ Single-run prompt: [45. Draft a Pre-Meeting Context Email for Tomorrow's External Meetings](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/email-communication.md#45-draft-a-pre-meeting-context-email-for-tomorrows-external-meetings)
