# 08. Weekly Standup Digest

**Category:** Meetings · **Time saved:** ~45 min/week (estimate — based on replacing the manual assembly of a weekly team summary from daily fragments) · **Difficulty:** ●○○

**What it does:** Collapses a week of standup notes (or async check-ins) into one digest: what shipped, what's blocked, who's overloaded, and what changed since last week. Managers get the signal without rereading five days of fragments.

**You need:** A `standups/` folder where daily notes or async updates accumulate (one file per day, or one running file).

## The prompt

```
Read all files in standups/ dated this week, plus last week's
digest in standups/digests/ if one exists.
Produce standups/digests/standup-digest-YYYY-MM-DD.md with:
1. SHIPPED — completed items, grouped by person.
2. BLOCKED — every blocker mentioned, with how many days it has
   now appeared (check last week's digest for repeats).
3. LOAD — anyone who mentioned being stretched, at capacity, or
   working on 3+ workstreams.
4. CHANGED — anything that contradicts last week's digest.
Max one page. No praise padding — just the signal.
```

## Setup (one time)

1. Create the folders; pick the team's drop convention (a daily file beats one giant running doc).
2. Run it once on a past week to calibrate the format before relying on it.

## Running it (each time)

1. Friday afternoon: run, skim, forward.
2. The BLOCKED repeat-counter is the highest-value line — a blocker at "day 8" is a management task, not a status item.

## Adapt it

- **Slack connector:** point it at a standup channel instead of files.
- **Monthly retro input:** feed four digests in and ask for patterns — recurring blockers and load trends.
- **Cross-team:** one digest per team folder, plus a combined leadership summary.

## Common failure + fix

**Failure:** The LOAD section over-fires on casual phrases ("busy week!") and under-fires on real overload stated dryly.
**Fix:** Calibrate with one example: add "LOAD example of a real signal: 'Tomás at 91% utilization' — a person named with a number or a named third workstream." Signal quality jumped immediately in testing.

---
→ Full guide: https://claudecoworktraining.com/guides/25-team-workflows/#08-weekly-standup-digest

→ Single-run prompt: [44. Compress a Week of Standup Notes into a Manager-Ready Digest Email](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/email-communication.md#44-compress-a-week-of-standup-notes-into-a-manager-ready-digest-email)
