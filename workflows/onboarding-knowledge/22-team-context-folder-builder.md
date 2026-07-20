# 22. Team Context Folder Builder

**Category:** Onboarding & Knowledge · **Time saved:** ~4 hrs one-time, then compounding (estimate — based on replacing the from-scratch drafting of team documentation; the payoff is every other workflow in this library working better) · **Difficulty:** ●●○

**What it does:** Builds your team's shared context folder — the about file, style guide, and glossary that every other workflow here depends on — by interviewing you and mining your existing documents, then drafting all three files for your review. The single highest-leverage setup task in this library.

**You need:** A folder of representative existing documents (a few reports, emails, or docs your team considers "how we sound"), and 20 minutes to answer questions.

## The prompt

```
I want to build a team context folder. Use the structure in
templates/context-file-examples/ as the target: about-your-team.md,
style-guide.md, glossary.md.
Step 1: Read the documents in samples/ and list what you can infer
about our team, writing style, and recurring terms.
Step 2: Interview me — ask up to 10 questions, one at a time, only
about what the documents DIDN'T tell you (hard rules, sensitive
data boundaries, term definitions you're unsure of).
Step 3: Draft all three files. Style rules must be evidenced by
the samples or my answers — no generic filler rules. The glossary
includes only terms a smart outsider would misunderstand.
Save drafts to team-context/. Mark anything you're unsure about
with "[CONFIRM]".
```

## Setup (one time)

This workflow IS the setup. Afterward: put the folder somewhere shared, and add "team-context changes go through [owner]" to the about file.

## Running it (each time)

Rerun quarterly as a refresh: "Read team-context/ and this quarter's new documents in samples/ — propose updates as a diff, don't rewrite."

## Adapt it

- **Department-specific overlay:** a sub-folder per team (marketing adds brand voice; finance adds data-handling rules).
- **Client-context version:** same interview flow to build a per-client context file for account teams.
- **Merger of two teams:** run on both teams' documents and ask for conflicts to resolve explicitly.

## Common failure + fix

**Failure:** Generic style rules that describe every company on earth ("be clear and professional") — a context folder full of filler teaches Cowork nothing.
**Fix:** The evidence rule: every style rule must trace to a sample or an interview answer. Our test against the Metamorfeus samples produced specific rules (banned words, date formats, the one-page default) because the rule forced specificity.

---
→ Full guide: https://claudecoworktraining.com/guides/25-team-workflows/#22-team-context-folder-builder

→ Single-run prompt: [63. Build a Team Context Folder from Existing Documents](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/team-workflows.md#63-build-a-team-context-folder-from-existing-documents)
→ Single-run prompt: [64. Quarterly Team Context Refresh as a Reviewable Diff](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/team-workflows.md#64-quarterly-team-context-refresh-as-a-reviewable-diff)
