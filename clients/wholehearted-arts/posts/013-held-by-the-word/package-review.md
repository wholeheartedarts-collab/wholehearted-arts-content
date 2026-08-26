# Content Package Review — 013 "Held by the Word- Be Still and Know that I am God"

Covers all three platform variants (LinkedIn, Instagram, Facebook) produced
for this topic together, per CLAUDE.md Step 10.

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal clear and matches brief | PASS | Art-collectors audience, faith/emotion/healing pillar, consistent across all three drafts (see each draft's "Angle used" section). |
| Every factual claim supported | PASS | Pulled directly from fact-check.md — no UNSUPPORTED claims. Psalm 37:7 and Psalm 46:10 both independently verified via WebSearch this run. |
| Balanced treatment (risks/drawbacks) | N/A | Not a topic with real drawbacks/risks to balance (art/faith reflection piece, not a claims-heavy AI-automation topic) — research.md's "Risks" section is about a scripture-attribution pitfall for the writer, not a reader-facing balance issue, and it was successfully avoided in all three drafts. |
| No fabricated facts/quotes/personal experiences | PASS | All scripture verified; no invented Agata anecdote beyond the catalog's own first-person text. |
| Client voice / avoid-list (no politics, no AI-slop) | PASS | Confirmed in each platform review. No political content anywhere in this package. |
| Platform-native structure per platform review | PASS | linkedin-review.md, instagram-review.md, facebook-review.md all PASS with no open items. |
| Hook strength and readability | PASS | Each hook grounded in the verified Psalm 37:7 text, sized correctly per platform (LinkedIn ~210, Instagram ~125). |
| Image relevant, original, style-guide consistent, correctly sized | **NEEDS HUMAN DECISION** | Image CDN blocked this run (confirmed via curl, `CONNECT tunnel failed, response 403`). No download/crop was possible — all three platforms will point to the same raw source image URL rather than platform-sized crops (LinkedIn 1200x627 / Instagram 1080x1350 / Facebook 1200x630). See `images/README-fallback.md`. Not a style-guide check either, since style-guide.json is still the placeholder (no reference images yet, per visual-style.md's documented status) and this is a real photo, not a generated one. |
| Alt text accurate and matches final image/post | **NEEDS HUMAN DECISION** | Alt text was written from the catalog's textual description only (`image_alt_from_site` is null for this entry) — not visually verified against the actual painting. Flagged in each `alt-text/[platform].md` file. Agata should confirm/correct before publishing. |
| Tags/mentions appropriate, minimal, no unwanted third-party tags | PASS | LinkedIn 3, Instagram 5 (at cap), Facebook 1 — none tag third parties. |
| Compliance constraints respected | PASS | No professional/medical/legal claims; no price stated anywhere despite the entry's active sale-price flag (correctly avoided per research.md). |
| No secrets/API keys/private info in output | PASS | Reviewed all files in this topic folder — no secrets present. |

## Summary of NEEDS HUMAN DECISION items (also going in the Step 13 email)

1. **Uncropped/unsized images.** All three platforms will use the same raw
   source image URL (not platform-sized crops) because the image CDN is
   blocked from this sandbox. Agata should review how it displays natively
   on each platform and consider swapping in a properly cropped version
   before or after publishing.
2. **Alt text not visually verified.** Written from the catalog's text
   description only. Agata should check it against the actual painting.
3. **Price is unresolved.** The entry carries an active `price_note` (ON
   SALE at snapshot time, $650 → $350). No draft states a price, but if
   Agata adds one when converting these from Buffer Ideas/draft into real
   posts, she should confirm the current price first.

## Status

All three platform reviews and the fact-check PASS with no FAILs. The two
NEEDS HUMAN DECISION items above are about image/alt-text provenance, not
content accuracy or brand-fit — the written content itself is ready for
human review. Nothing in this package is approved, scheduled, or published
by this run.
