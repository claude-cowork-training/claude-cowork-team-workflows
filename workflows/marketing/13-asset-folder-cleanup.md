# 13. Asset Folder Cleanup

**Category:** Marketing · **Time saved:** ~3 hrs/month (estimate — based on replacing the recurring "where is the final version" hunt across a shared drive) · **Difficulty:** ●○○

**What it does:** Points at a messy shared folder — inconsistent names, near-duplicates, "FINAL_v2_ACTUAL" files — and produces a rename-and-move plan: proposed structure, duplicate list with a recommended keeper, and orphans needing a human decision. Plan first, changes only after your approval.

**You need:** The messy folder (start with a copy), and a `naming-convention.md` describing your target scheme (or let the first run propose one).

## The prompt

```
Read every filename and skim the contents of assets/ (do not
modify anything yet).
Produce cleanup-plan.md:
1. Proposed folder structure (by campaign/format/date per
   naming-convention.md).
2. Rename table: current name → proposed name, one row per file.
3. Duplicates and near-duplicates: group them, recommend which to
   keep and why (newest, most complete, or explicitly marked
   final), and list the rest for archive.
4. "Needs a human": anything whose purpose or version you can't
   determine — never guess which version is current.
Wait for my approval before executing any renames or moves.
```

## Setup (one time)

1. Copy the messy folder — practice on the copy first.
2. Write `naming-convention.md` (even 4 rules beats none), or adopt what the first plan proposes.

## Running it (each time)

1. Run, review the plan — especially the duplicate keeper choices — then say "execute the approved plan".
2. Monthly cadence keeps it a 10-minute review instead of a quarterly excavation.

## Adapt it

- **Sales collateral version:** same flow on the proposals folder; add "flag anything with outdated pricing".
- **Photo/video assets:** organize by campaign and shoot date from file metadata.
- **Ongoing enforcement:** weekly run on just the folder's new arrivals.

## Common failure + fix

**Failure:** Auto-picking the wrong "final" version — the file named FINAL is often older than an unlabeled v2.
**Fix:** The plan-then-approve gate and the "never guess which version is current" rule. Tested on the Metamorfeus messy-folder dataset (two proposal versions, one marked superseded): the plan correctly kept v2 and flagged the ambiguous invoice pair for a human instead of choosing.

---
→ Full guide: https://claudecoworktraining.com/guides/25-team-workflows/#13-asset-folder-cleanup

→ Single-run prompt: [53. Project Folder Cleanup Plan with Rename and Archive Table](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/project-management.md#53-project-folder-cleanup-plan-with-rename-and-archive-table)
