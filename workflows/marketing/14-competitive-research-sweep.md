# 14. Competitive Research Sweep

**Category:** Marketing · **Time saved:** ~3 hrs/month (estimate — based on replacing a recurring manual research-and-summarize session) · **Difficulty:** ●●○

**What it does:** Runs a structured monthly sweep of your tracked competitors — collected notes, saved pages, and (if enabled) web research — and produces a briefing your team will actually read: what changed, what it means for you, and what to do about it. Delta-focused: it reports changes since last month, not a re-description of everyone.

**You need:** A `competitors/` folder with one subfolder per competitor (notes, saved pages, past briefings), and last month's briefing as the baseline.

## The prompt

```
Read every competitor subfolder in competitors/ and last month's
briefing in competitors/briefings/.
Produce this month's briefing:
1. Per competitor: WHAT CHANGED since last month (pricing,
   positioning, offers, notable content). If nothing changed,
   write one line saying so — do not pad.
2. SO WHAT: max 3 implications for us, each tied to a specific
   change above.
3. RECOMMENDED MOVES: max 2, concrete.
Separate facts from inference: anything not directly evidenced in
the folder is labeled "(inference)". Cite the source file or URL
for every factual claim.
Save as competitors/briefings/competitive-brief-YYYY-MM.md.
```

## Setup (one time)

1. One subfolder per tracked competitor; make dropping in screenshots/notes a team habit.
2. Write the first baseline briefing manually or via a first run — deltas need a starting point.

## Running it (each time)

1. First business day of the month: run, verify the "(inference)" labels, share.
2. Nothing-changed months are the feature, not a failure — a 5-line briefing keeps the habit cheap.

## Adapt it

- **Web-enabled:** with browsing available, add "check each competitor's pricing and blog pages for changes" — keep the citation rule.
- **Win/loss overlay:** add your sales team's win/loss notes to the inputs.
- **Weekly, single competitor:** for a launch period, run daily deltas on just one.

## Common failure + fix

**Failure:** Confident competitive "facts" that are actually pattern-matched inference from thin notes.
**Fix:** The fact/inference separation with citations. Tested on the Metamorfeus research-brief dataset (two fictional competitors, SentinelOps and PlantPulse): user-review claims about one competitor were correctly labeled with their two-review source rather than stated as market truth.

---
→ Full guide: https://claudecoworktraining.com/guides/25-team-workflows/#14-competitive-research-sweep

→ Single-run prompt: [31. Monthly Competitive Change Briefing from a Competitor Notes Folder](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/research-summarization.md#31-monthly-competitive-change-briefing-from-a-competitor-notes-folder)
→ Single-run prompt: [32. Single-Competitor Deep Dive Brief with Per-Claim File Citations](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/research-summarization.md#32-single-competitor-deep-dive-brief-with-per-claim-file-citations)
