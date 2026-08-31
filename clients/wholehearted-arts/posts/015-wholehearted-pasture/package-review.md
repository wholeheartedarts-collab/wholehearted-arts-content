# Package Review — "Wholehearted Pasture" (015)

Full pre-publish review gate covering all three platform variants together.

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal clear and match brief | PASS | Art collectors / faith audience; takeaway (service as posture, not scale) consistent across all three platforms, each in its own register. |
| Every factual claim supported | PASS | Per fact-check.md — all scripture quotes and product facts SOURCED; one interpretive framing item reviewed and accepted with rationale, no UNSUPPORTED claims. |
| Balanced treatment of real risks/drawbacks | N/A | Not a topic with meaningful counterarguments (a scripture/art-meaning piece, not a claims-based argument) — research.md's limitations section is about content risk (thin narrative, Psalm 23 conflation), both of which were successfully avoided in all three drafts. |
| No fabricated facts, quotations, personal experiences, results | PASS | No invented studio story, backstory, or personal anecdote beyond the catalog's own thin description, per research.md's explicit caution. |
| Client voice / avoid-list (no politics, no AI-slop) | PASS | Confirmed in each platform review; no politics anywhere in the package. |
| Platform-native structure / format requirements | PASS | Confirmed via linkedin-review.md, instagram-review.md, facebook-review.md — all three PASS with no revisions needed. |
| Hook strength and readability | PASS | Each hook is platform-length-appropriate and distinct (not the same hook copy-pasted across platforms). |
| Image relevant, original, consistent with style guide, correctly sized | **NEEDS HUMAN DECISION** | Source image could not be downloaded this run (CDN blocked — see images/README-fallback.md). No platform-sized crops exist; all three platforms reference the same uncropped raw `image_url`. It is the real painting photo (not AI-generated), so "original" and "relevant" are satisfied, but "correctly sized" is not met for any platform this run. |
| Alt text accurate, matches final image and post | **NEEDS HUMAN DECISION** | Alt text was written from the catalog's thin textual description only (`image_alt_from_site` is null for this entry) — not visually verified against the actual image, clearly flagged in all three alt-text files. Agata should confirm/correct against the real painting before publishing. |
| Tags/mentions appropriate, minimal, no unwanted third-party tags | PASS | LinkedIn: none. Instagram: 5 (at cap, relevant mix). Facebook: 1. No third parties tagged. |
| Compliance constraints from client profile respected | PASS | No professional/medical/legal claims; no price claim made anywhere in the package (none of the three drafts state a price). |
| No secrets/API keys/private information in output | PASS | Nothing beyond public painting/product data and public scripture text. |

## NEEDS HUMAN DECISION items (both stem from the same egress block)

1. **Uncropped image.** All three platforms currently point to the same raw
   source photo URL rather than a platform-sized crop (LinkedIn 1200x627 /
   Instagram 1080x1350 / Facebook 1200x630). Buffer's own servers can still
   fetch and attach this URL independently of this sandbox, so staging in
   Buffer isn't blocked — but the visual framing per platform hasn't been
   optimized this run.
2. **Alt text not visually verified.** Written from catalog text only; please
   check it against the actual painting before this package is approved.

Both are recorded here, at the top of the Step 13 email, and in the final
run summary, per the run's own hard rules.

## Overall verdict

**PASS with two flagged NEEDS HUMAN DECISION items** (both caused by the
same known, expected egress block, not a content-quality problem). Package
may proceed to `review-ready` and Buffer staging; must not move past
`review-ready` without Agata's explicit decision on the two items above.
