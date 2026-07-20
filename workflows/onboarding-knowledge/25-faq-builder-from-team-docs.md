# 25. FAQ Builder from Team Docs

**Category:** Onboarding & Knowledge · **Time saved:** ~2 hrs/month (estimate — based on replacing the repeated answering of the same internal questions, one Slack thread at a time) · **Difficulty:** ●○○

**What it does:** Reads your team-context folder and a collected pile of actually-asked questions (from chat exports, onboarding sessions, or a running list) and produces a maintained FAQ: each answer sourced to a team document, each unanswerable question flagged as a documentation gap. The FAQ writes itself from what people really ask.

**You need:** Your `team-context/` folder, a `questions/` folder or file where the team dumps real questions, and the existing FAQ if one exists.

## The prompt

```
Read team-context/ (all of it), questions/, and the existing
faq.md if present.
Produce faq-update-YYYY-MM-DD.md:
1. For each new question in questions/: a concise answer sourced
   ONLY from team-context documents, with the source file named
   under each answer. If no document answers it, list it under
   "DOCUMENTATION GAPS" with a suggested home for the answer.
2. Group Q&As by theme; merge duplicate questions but keep the
   phrasing people actually used.
3. STALE CHECK: flag existing FAQ answers that contradict current
   team-context files.
Answers must not go beyond what the documents say — a wrong
confident answer in an FAQ is worse than a gap.
```

## Setup (one time)

1. Create the questions drop point and make "if you had to ask it, drop it in" the team norm.
2. Seed with the questions from your last new-hire onboarding — they're the FAQ's real table of contents.

## Running it (each time)

1. Run monthly; merge the update into the main FAQ after review.
2. The DOCUMENTATION GAPS list is the real output — each gap is a 10-minute writing task that permanently deletes a recurring question.

## Adapt it

- **Client FAQ:** run on a client-facing folder plus questions from client emails.
- **Sales objection bank:** questions/ becomes objections heard on calls; answers source from your positioning docs.
- **Feeds workflow 22:** recurring gaps in the same area signal a missing team-context file, not just a missing FAQ line.

## Common failure + fix

**Failure:** Answers that smooth over document silence — the FAQ confidently states a policy the team never wrote down, and it becomes de facto policy by accident.
**Fix:** The documents-only rule plus per-answer sourcing. Tested against the Metamorfeus context folder with 12 synthetic new-hire questions: 8 answered with correct sources, 4 correctly landed in DOCUMENTATION GAPS — including one ("who approves discounts?") whose answer existed only in an internal-only pricing file, which the rule correctly kept out of the FAQ.

---
→ Full guide: https://claudecoworktraining.com/guides/25-team-workflows/#25-faq-builder-from-team-docs

→ Single-run prompt: [67. Build a Sourced Team FAQ from Actually-Asked Questions](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/team-workflows.md#67-build-a-sourced-team-faq-from-actually-asked-questions)
→ Single-run prompt: [68. Answer New-Hire Questions from the Context Folder Only](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/team-workflows.md#68-answer-new-hire-questions-from-the-context-folder-only)
