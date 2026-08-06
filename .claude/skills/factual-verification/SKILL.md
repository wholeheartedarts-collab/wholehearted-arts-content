---
name: factual-verification
description: Verify that every factual claim, statistic, quotation, or example in a draft post is supported by the research sources before the post moves to review or publishing. Use after a post draft exists and before content-package-review.
---

# Factual Verification

## Purpose

Catch fabrication or drift between research and the final post. Research
can be accurate while a later draft quietly overstates, misattributes, or
invents something in service of a better hook — this skill exists to
catch that.

## Process

1. Read the draft post (`linkedin-post.md`) and the research package
   (`research.md`, `sources.md`) for the same topic folder.
2. For every factual claim, statistic, named example, or quotation in the
   draft, confirm it traces back to a specific source in `sources.md`.
3. Flag anything that:
   - Has no matching source.
   - Overstates what the source actually says (e.g., a source says
     "some clinics reported faster intake" and the draft says "proven to
     cut wait times in half").
   - Uses a real statistic but drops important context (date, sample
     size, geography) in a misleading way.
   - Presents a fabricated customer story, personal anecdote, or result
     as if real. Client-specific claims (about Agata's own art, books, or
     AI-automation work) must come from the human, not be invented.

## Output

Append a short **Fact-check** section to `review.md` (or create it if
`content-package-review` hasn't run yet) listing each claim and its
status: `SOURCED`, `NEEDS SOFTENING`, or `UNSUPPORTED — remove or confirm
with human`.

## Hard rule

If any claim is `UNSUPPORTED`, the package cannot pass
[[content-package-review]] until it's fixed or the human explicitly
accepts the risk in writing.
