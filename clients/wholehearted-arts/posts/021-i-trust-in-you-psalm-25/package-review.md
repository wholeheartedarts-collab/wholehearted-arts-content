# Full package review — 021 "I Trust In You My God — Psalm 25"

Covers LinkedIn, Instagram, and Facebook variants together.

| Check | Verdict | Notes |
|---|---|---|
| Topic, audience, takeaway, tone, goal clear and match brief | PASS | Faith/prayer pillar, art-collector audience, clear across all three platforms. |
| Every factual claim/statistic/example supported | PASS | Pulled from fact-check.md — no UNSUPPORTED claims in any draft. |
| Balanced treatment where topic has real risks/drawbacks | N/A | Devotional art topic, not an advice/claims topic with real drawbacks to balance (unlike the AI-automation pillar). |
| No fabricated facts, quotations, personal experiences, results | PASS | No invented Agata backstory; scripture quoted verbatim and verified; painting description drawn directly from catalog. |
| Client voice and avoid-list rules followed | PASS | No politics; no AI-slop phrasing; voice matches brand-voice.md across all three drafts. |
| Platform-native structure / current format requirements met | PASS | Pulled from linkedin-review.md, instagram-review.md, facebook-review.md — all three PASS with no open revisions. |
| Hook strength and readability | PASS | Each platform has its own distinct, grounded hook (not reused across platforms). |
| Image relevant, original, consistent with style-guide.json, correctly sized | NEEDS HUMAN DECISION | Image is relevant (the actual painting) and not a copied reference, but it is the **raw, uncropped `primary_image_url`** for all three platforms — not cropped to style-guide.json's per-platform dimensions (LinkedIn 1200x627, Instagram 1080x1350, Facebook 1200x630), because the image CDN (images.squarespace-cdn.com) is blocked by this sandbox's egress policy (one failed download attempt, not retried per run instructions). Buffer's own servers will fetch the URL independently and may display it uncropped/letterboxed differently per platform. A human should re-crop once local image access is available. |
| Alt text accurate, matches final image and post | NEEDS HUMAN DECISION | Alt text (see `alt-text/`) was written from the catalog's product description and title only — it was **not visually verified** against the actual image file, since the image could not be downloaded in this run. It is a reasonable, non-speculative description grounded in real product data, but a human who can view the image directly should confirm or correct it. |
| No mockup selected | NEEDS HUMAN DECISION | This entry has no `chosen_images` block (consistent with every Studio-collection entry observed so far — none currently have curated mockups). Per run instructions, the flat/primary product photo was used, and no draft or alt text asserts a room-mockup scene. A human should review this painting's 7 product photos and add a `chosen_images` block to the catalog if one is a suitable room mockup, for future runs. |
| Tags/mentions appropriate, minimal, no unwanted third-party tagging | PASS | LinkedIn: none. Instagram: 5 relevant tags, no third parties. Facebook: 1 brand tag. |
| Compliance constraints from client profile respected | PASS | No compliance constraints defined for this content pillar (art, not AI-automation). |
| No secrets, API keys, private information anywhere in package | PASS | Verified — no keys or secrets in any file. |

## Summary verdict

**No FAIL items.** Three items are **NEEDS HUMAN DECISION**, all stemming from the same root cause (image CDN egress block in this sandbox) plus the catalog's lack of a curated mockup for this entry:

1. All three platform images are the raw, uncropped source photo, not platform-sized crops.
2. Alt text was written from catalog text only, not visually verified.
3. No `chosen_images`/mockup exists for this painting — human should review and add one for future runs.

None of these are fabrication, factual, or voice/tone problems — the text content of all three drafts is fully supported and platform-review-passed. Package is presented as `review-ready`, not `approved`.
