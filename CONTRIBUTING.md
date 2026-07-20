# Contributing a workflow

New workflows are welcome — the goal is a library teams actually run, so the bar is "tested and real," not "sounds plausible."

## The rules (all four required)

1. **Recurring.** Weekly or monthly cadence. One-off tasks belong in a prompt library, not here.
2. **Cowork-native.** The workflow must be demonstrably better in Cowork than in a chat window — file access, multi-step execution, or output files. If the prompt would work identically pasted into chat, it doesn't qualify.
3. **Tested.** You ran it in Claude Cowork at least once, end to end, before opening the PR. Say so in the PR description and note anything that surprised you.
4. **Synthetic data only.** No real company names, client data, or personal information in examples. You can reuse our fictional company (Metamorfeus — see any workflow file) or invent your own, but keep it fictional and say so.

## How

1. Copy [`templates/workflow-template.md`](templates/workflow-template.md).
2. Fill every section — including **Common failure + fix** (the section reviewers check first) and a time-saved estimate **labeled as an estimate** with a one-line basis.
3. Name the file `NN-kebab-case-name.md` using the next free number, place it in the matching category folder, and add a row to the README table.
4. Add a line to `CHANGELOG.md`.
5. Open a PR. We respond within 48 hours.

## Fixes and improvements

Typos, clearer setup steps, better failure notes — just open a PR, no template needed. If a prompt stopped working because Cowork's behavior changed, that's the most valuable PR of all: describe what changed and include your fixed prompt.

By contributing you agree your contribution is licensed under [CC BY 4.0](LICENSE).
