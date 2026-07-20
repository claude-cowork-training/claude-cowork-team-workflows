# 24. Playbook Writer

**Category:** Onboarding & Knowledge · **Time saved:** ~1.5 hrs per playbook (estimate — based on replacing the documentation session nobody schedules, which is why the process lives in one person's head) · **Difficulty:** ●●○

**What it does:** Turns how one person actually does a recurring task into a playbook anyone can run: trigger, inputs, steps, standards, and known failure modes — extracted by interviewing the task owner and reading the artifacts the task produces. The bus-factor killer.

**You need:** The task owner (20 minutes), 2–3 past outputs of the task as examples, and a `playbooks/` folder in your team context.

## The prompt

```
I want to document a recurring task as a playbook. The past
outputs are in examples/.
Step 1: Read the examples and describe the task as you understand
it: cadence, inputs, output format, quality standards you can
infer.
Step 2: Interview me (I'm the task owner) — up to 8 questions, one
at a time, prioritizing: what triggers it, where inputs live, what
"good" looks like, what goes wrong, and what you got wrong in
Step 1.
Step 3: Write the playbook using this structure: Trigger · Owner ·
Inputs (exact locations) · Output (name, format, destination) ·
Standards · Known failures and what to do.
It must pass the colleague test: someone who has never done this
task could run it from the playbook alone. Flag anything still
ambiguous.
Save as team-context/playbooks/[task-name]-playbook.md.
```

## Setup (one time)

1. List your team's recurring tasks; rank by bus-factor risk (one owner + business-critical first).
2. Create `playbooks/` in the team-context folder.

## Running it (each time)

1. One playbook per session; the owner answers the interview honestly, including the embarrassing workarounds — those ARE the playbook.
2. Colleague test for real: someone else runs the task from the doc next cycle.

## Adapt it

- **Handover mode:** run it during someone's notice period across all their tasks.
- **Workflow conversion:** a finished playbook is 80% of a Cowork prompt — its Inputs/Output/Standards sections map straight onto the workflow template in this repo.
- **Client-facing SOPs:** same flow for processes you deliver to clients.

## Common failure + fix

**Failure:** Happy-path playbooks — the steps when everything works, missing the "when the export is late, use last week's and mark it" reality that makes the task actually runnable.
**Fix:** The interview explicitly asks what goes wrong, and the structure mandates a known-failures section. In testing (documenting the Metamorfeus weekly digest against its real playbook), the interview step surfaced two failure rules the inferred draft had missed.

---
→ Full guide: https://claudecoworktraining.com/guides/25-team-workflows/#24-playbook-writer

→ Single-run prompt: [66. Write a Playbook for a Recurring Task from Its Past Outputs](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/team-workflows.md#66-write-a-playbook-for-a-recurring-task-from-its-past-outputs)
