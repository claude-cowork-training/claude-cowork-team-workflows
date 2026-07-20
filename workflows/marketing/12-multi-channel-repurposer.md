# 12. Multi-Channel Repurposer

**Category:** Marketing · **Time saved:** ~2 hrs per piece (estimate — based on replacing the manual reformat of one long-form piece into 4–5 channel versions) · **Difficulty:** ●○○

**What it does:** Takes one finished long-form piece (blog post, case study, webinar summary) and produces formatted, on-brand versions for each of your channels — email, LinkedIn, X/short-form, and a blog excerpt — as separate ready-to-paste files, not one wall of text.

**You need:** A `content/` folder with the source piece, your brand style guide, and one past example per channel that performed well.

## The prompt

```
Read content/source/[PIECE].md, team-context/style-guide.md, and
the examples in content/channel-examples/.
Create one file per channel in content/repurposed/[PIECE]/:
- email.md — subject line + 120-word body + one CTA
- linkedin.md — 150–200 words, hook in line one, no hashtag spam
- short.md — 3 variants under 280 characters
- excerpt.md — 100-word blog teaser + suggested internal links
Each version must match its channel example's voice, contain one
idea (not a summary of everything), and preserve any claims
EXACTLY as sourced — no strengthening numbers or adding
superlatives that aren't in the original.
```

## Setup (one time)

1. Create `channel-examples/` with one strong past post per channel — this teaches voice better than any instruction.
2. Agree the folder-per-piece output convention with whoever schedules posts.

## Running it (each time)

1. Drop the finished source piece in, run, review each file against its channel example.
2. The 3 short-form variants exist so you pick, not settle.

## Adapt it

- **Localization pass:** add a per-language output ("also produce a Spanish LinkedIn version, same rules").
- **Sales enablement:** add "one-paragraph version for account managers to paste into client emails".
- **Video piece:** source from a transcript instead — add "ignore filler and verbal tics".

## Common failure + fix

**Failure:** Claim drift — "clients report saving hours" becomes "saves teams 10+ hours" by the third repurpose.
**Fix:** The claims-preservation rule in caps. Tested with a Metamorfeus case-study draft containing a client-reported figure: with the rule, all five outputs carried the exact original phrasing and its "client-reported" qualifier.

---
→ Full guide: https://claudecoworktraining.com/guides/25-team-workflows/#12-multi-channel-repurposer
