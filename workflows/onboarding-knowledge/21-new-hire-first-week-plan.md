# 21. New Hire First-Week Plan

**Category:** Onboarding & Knowledge · **Time saved:** ~2 hrs per hire (estimate — based on replacing the manager's manual assembly of a first-week schedule and reading list) · **Difficulty:** ●○○

**What it does:** Generates a customized first-week plan for a new hire from your onboarding checklist, team-context folder, and the role description: day-by-day schedule, reading list in priority order, who to meet and why, and the first small real task. Consistent onboarding without the manager rebuilding it every time.

**You need:** A `team-context/` folder (see [samples](../../templates/context-file-examples/)), an `onboarding/checklist.md` of universal steps, and the role description for this hire.

## The prompt

```
Read team-context/, onboarding/checklist.md, and
onboarding/roles/[ROLE].md.
Create onboarding/plans/[NAME]-week-1.md:
1. Day-by-day schedule for week one — checklist items placed
   sensibly (accounts before tools, context before clients).
2. Reading list from team-context/, ordered by relevance to this
   role, one line each on why it matters.
3. People to meet: from about-your-team.md, who this role works
   with and what to ask them.
4. A first real task — small, role-relevant, completable by
   Friday, drawn from the role file's responsibilities.
Only reference files and people that actually appear in the
folders. If the role file is missing detail, flag it — don't
invent responsibilities.
```

## Setup (one time)

1. Build the team-context folder (workflow 22 does this) and a one-page role file per role.
2. Write `checklist.md` once — every plan reuses it.

## Running it (each time)

1. Run the week before the start date; manager reviews, adjusts the meetings, done.

## Adapt it

- **30/60/90 version:** extend to a full ramp plan with milestones per month.
- **Contractor version:** compressed to day one, access-and-context only.
- **Buddy pack:** add "a one-page brief for the onboarding buddy: what to cover in each check-in".

## Common failure + fix

**Failure:** Invented meetings and responsibilities when the role file is thin — the new hire's plan references duties nobody agreed to.
**Fix:** The only-what-exists rule. Tested against the Metamorfeus team-context folder for a fictional junior-analyst hire: the plan drew meetings only from the four real team leads and flagged the thin role file instead of padding it.

---
→ Full guide: https://claudecoworktraining.com/guides/25-team-workflows/#21-new-hire-first-week-plan

→ Single-run prompt: [61. Generate a New Hire's First-Week Plan from Team Docs](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/team-workflows.md#61-generate-a-new-hires-first-week-plan-from-team-docs)
→ Single-run prompt: [62. Turn a First-Week Plan into a 30/60/90 Ramp Plan](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/team-workflows.md#62-turn-a-first-week-plan-into-a-306090-ramp-plan)
