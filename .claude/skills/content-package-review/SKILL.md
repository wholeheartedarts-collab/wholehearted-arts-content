---
name: content-package-review
description: Run the full pre-publish review gate over a complete content package (research, post, image, alt text) before it's presented for human approval. Use last, after all other skills for a topic have run.
---

# Content Package Review

This is the final gate before a package is presented to the human for
approval. It's broader than [[linkedin-review]] (platform fit only) —
this checks the whole package.

## Checklist

- Topic, audience, takeaway, tone, and goal are clear and match the brief.
- Every factual claim/statistic/example is supported — pull the result
  from [[factual-verification]]; do not re-derive it from scratch.
- Balanced treatment where the topic has real risks or drawbacks (check
  research.md's limitations section made it into the post where relevant).
- No fabricated facts, quotations, personal experiences, or results.
- Client voice and avoid-list rules followed (no politics; no AI-slop
  phrasing) — see [[brand-voice]].
- Platform-native structure and current LinkedIn format requirements met
  — pull from [[linkedin-review]].
- Hook strength and readability.
- Image is relevant to the actual finished post, original (not a copied
  reference), consistent with `style-guide.json`, and correctly sized.
- Alt text is accurate and matches the final image and post.
- Tags/mentions are appropriate, minimal, not forced, and no unwanted
  tagging of third parties.
- Compliance constraints from the client profile are respected.
- No secrets, API keys, or private information appear anywhere in the
  output package.

## Output

Save/update `clients/[client-slug]/posts/[NNN-topic-slug]/review.md` with
a table: check → verdict → notes. Verdicts are one of:

- **PASS**
- **NEEDS HUMAN DECISION** — not necessarily wrong, but a judgment call
  only the client should make (e.g., a provisional-voice choice, a
  borderline claim, an ambiguous CTA).
- **FAIL** — must be fixed before this package can be presented as
  ready.

## Hard rule

If any check is FAIL, stop and fix it (looping back to the relevant
skill) before presenting the package. If any check is NEEDS HUMAN
DECISION, present the package anyway but call out every such item
explicitly and clearly in the summary — do not bury them. Nothing is
published or scheduled from this skill; see [[publishing-handoff]].
