# 23. Glossary Extractor

**Category:** Onboarding & Knowledge · **Time saved:** ~2 hrs one-time per domain (estimate — based on replacing the manual "what does this acronym mean" archaeology every new hire performs) · **Difficulty:** ●○○

**What it does:** Mines a folder of your team's real documents for internal shorthand — acronyms, nicknames, terms-of-art — and drafts glossary entries with the definition inferred from usage, a confidence label, and the source lines it appeared in. Turns tribal knowledge into a file.

**You need:** A `samples/` folder of representative internal documents (the messier and more real, the better), and your existing glossary if one exists.

## The prompt

```
Read every document in samples/ and the existing
team-context/glossary.md if present.
Find every term a smart new hire would not understand: acronyms,
internal nicknames, product/process names, terms used with a
non-obvious specific meaning.
For each NEW term (not already in the glossary), draft an entry:
- The term
- Definition inferred from how it's used, with confidence:
  CONFIDENT (usage makes it unambiguous) or GUESS (verify with
  the team)
- 1–2 source quotes showing it in use
Exclude standard industry terms any professional would know.
Output as glossary-additions-YYYY-MM-DD.md for review — do not
edit the main glossary directly.
```

## Setup (one time)

1. Fill `samples/` with 10–20 real internal docs across functions.
2. Decide who reviews additions before they merge into the main glossary.

## Running it (each time)

1. Run quarterly, or after any big new project spawns new vocabulary.
2. Review the GUESS entries as a team — the disagreements are usually the most valuable definitions to pin down.

## Adapt it

- **Client-specific glossary:** run on one client's folder — their acronyms, for account handovers.
- **Style-rule mining:** same mechanic, extracting recurring formats instead of terms ("we always structure digests as...").
- **Deprecation pass:** add "flag glossary terms that no longer appear in any recent document".

## Common failure + fix

**Failure:** Confident wrong definitions — a term used twice gets a plausible definition that's subtly off, and the glossary now teaches new hires the wrong thing.
**Fix:** The confidence labels and source quotes. Tested on the Metamorfeus document set: "the board numbers" (a term with a very specific internal meaning — three metrics, fixed order) came back CONFIDENT with correct sources, while a term appearing once was properly labeled GUESS.

---
→ Full guide: https://claudecoworktraining.com/guides/25-team-workflows/#23-glossary-extractor

→ Single-run prompt: [65. Extract a Team Glossary from Real Internal Documents](https://github.com/claude-cowork-training/claude-cowork-prompts/blob/main/prompts/team-workflows.md#65-extract-a-team-glossary-from-real-internal-documents)
