# Package review: "In the Cradle of Faith" (012)

Covers all three platform variants together, per CLAUDE.md's
multi-platform convention.

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal clear and match brief | PASS | Faith-as-refuge theme, art-collector audience, consistent across all three drafts. |
| Every factual claim supported | PASS | See `fact-check.md` — two invented process claims caught and corrected during fact-check; none remain unsupported. |
| Balanced treatment of real risks/drawbacks | N/A | Devotional/art topic with no drawbacks or counterarguments to represent (per research.md). |
| No fabricated facts, quotations, personal experiences, results | PASS | Confirmed in fact-check.md; no scripture claimed to be inscribed in the painting; no invented backstory. |
| Client voice / avoid-list (no politics, no AI-slop) | PASS | All three platform reviews passed voice and no-politics checks. |
| Platform-native structure per platform review | PASS | linkedin-review.md, instagram-review.md, facebook-review.md all PASS with no revisions outstanding. |
| Hook strength and readability | PASS | Each hook checked against its platform's character-cutoff rule in its own review file. |
| Image relevant, original, style-guide-consistent, correctly sized | **NEEDS HUMAN DECISION** | This is a real photo of Agata's own painting (not AI-generated), which is correct and relevant. However, the image CDN (`images.squarespace-cdn.com`) was blocked by the sandbox egress proxy this run — confirmed via a single `curl` test (`CONNECT tunnel failed, response 403`), not retried per instructions. No local download/crop was possible, so **no per-platform sizing was done** (no LinkedIn 1200x627, Instagram 1080x1350 portrait, or Facebook 1200x630 crops exist for this topic). Per run instructions this is a sanctioned fallback, not a run failure: the catalog's raw public `image_url` is passed directly to Buffer instead (Buffer's servers fetch it independently of this sandbox). Flagging as NEEDS HUMAN DECISION because Agata should know the images she'll see in Buffer are the full uncropped source photo, not platform-optimized crops, and may want to crop/replace them herself before publishing. See `images/README-fallback.md`. |
| Alt text accurate and matches final image/post | **NEEDS HUMAN DECISION** | Alt text (see `alt-text/*.md`) was written from the catalog's textual description only, since the image itself could not be visually verified this run (same CDN block as above) and the catalog's own `image_alt_from_site` field is `null` for this entry. Clearly flagged as unverified in each alt-text file. Agata should confirm/correct against the actual painting before publishing. |
| Tags/mentions appropriate, minimal, no unwanted third-party tagging | PASS | 2 tags (LinkedIn), 5 tags at cap (Instagram), 1 tag (Facebook) — all relevant, no third parties tagged. |
| Compliance constraints from profile respected | PASS | No professional/medical/legal claims; price ($400) matches catalog with no `price_note` flag, so no on-sale/discount claim risk. |
| No secrets, API keys, or private info anywhere in package | PASS | Reviewed all files in this topic folder; none present. |

## Summary

**Two NEEDS HUMAN DECISION items, both stemming from the same root cause**
(image CDN blocked this run): the Buffer-staged images will be the raw,
uncropped source photo rather than platform-sized crops, and the alt text
is written from catalog text only, not verified against the actual image.
Both are flagged clearly here, in `status.json`, the final run summary,
and the Step 13 email. No FAIL items — nothing else blocks presenting this
package as review-ready.
