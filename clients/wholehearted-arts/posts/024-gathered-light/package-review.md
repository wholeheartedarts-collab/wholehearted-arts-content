# Content package review — 024 "Gathered Light"

Covers all three platform variants together (LinkedIn, Instagram, Facebook).

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal clear and match brief | PASS | Art pillar, art-collector audience, faith/healing angle, matches brief.md. |
| Every factual claim supported | PASS | See fact-check.md — no UNSUPPORTED claims. |
| Balanced treatment of real risks/drawbacks | N/A | Not a topic with risk/drawback balance requirements (art piece, not an AI-automation claim). |
| No fabricated facts/quotes/experiences/results | PASS | Catalog description quoted verbatim; scripture verified independently; no sitter identity or personal story invented (per research.md Risks section). |
| Client voice / avoid-list followed | PASS | No politics; no AI-slop phrasing across all three drafts (see platform reviews). |
| Platform-native structure met | PASS | See linkedin-review.md / instagram-review.md / facebook-review.md — all PASS. |
| Hook strength and readability | PASS | All three hooks grounded in catalog language, correctly sized per platform. |
| Image relevant, original, style-consistent, correctly sized | **NEEDS HUMAN DECISION** | Image is a real, human-verified room mockup (not AI-generated) — relevant and appropriate. But it could NOT be downloaded/cropped to platform dimensions this run (CDN egress blocked, confirmed via one failed attempt — see images/README-source-image.md). The raw uncropped source URL was used for all three platforms instead of platform-sized crops. A human should verify it displays acceptably in Buffer's composer for each platform, or crop it locally. |
| Alt text accurate, matches final image and post | **NEEDS HUMAN DECISION** | Alt text was written from the catalog's product description and `chosen_images.note`, not from direct visual inspection (image could not be downloaded this run). A human should confirm the alt text actually matches the image before it goes out — see alt-text/*.md. |
| Tags/mentions appropriate, minimal, no unwanted third-party tagging | PASS | LinkedIn 2 tags, Instagram 5 tags (at the cap, all relevant), Facebook 1 tag — no third parties tagged. |
| Compliance constraints from profile respected | PASS | No compliance constraints apply to this topic (art piece, not AI-automation service claim). |
| No secrets/API keys/private info in output | PASS | Confirmed — no keys or private data in any file this run. |

## NEEDS HUMAN DECISION items (summary)

1. **Image not downloaded/cropped this run.** Egress to
   `images.squarespace-cdn.com` is blocked in this sandbox (confirmed
   via one failed Python download attempt, not retried). All three
   platforms use the raw, uncropped `chosen_images.mockup_url` passed
   directly to Buffer. A human should confirm it renders acceptably per
   platform, or download/crop it locally to LinkedIn 1200x627 /
   Instagram 1080x1350 / Facebook 1200x630.
2. **Alt text not visually verified.** Written from the catalog's
   description and `chosen_images.note` rather than direct image
   inspection, for the same egress reason. A human should confirm
   accuracy before publishing.

No other open items. All platform-fit reviews and the fact-check
passed cleanly.
