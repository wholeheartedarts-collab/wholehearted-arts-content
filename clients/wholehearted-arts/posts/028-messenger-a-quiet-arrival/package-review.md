# Full package review — 028 "Messenger" (LinkedIn + Instagram + Facebook)

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal clear and match brief | PASS | Art-collector audience, faith/reflection pillar, "quiet arrival" angle consistent across all three drafts. |
| Every factual claim supported | PASS | Pulled from fact-check.md — no UNSUPPORTED claims across any platform. |
| Balanced treatment of real risks/drawbacks | PASS (N/A) | This topic (devotional art reflection) has no meaningful counterargument/risk to balance, per research.md; not a claims-heavy topic. |
| No fabricated facts/quotes/personal experiences/results | PASS | No third-party story or invented statistic in any draft; painting facts from the live catalog; scripture verified via WebSearch. |
| Client voice and avoid-list rules followed | PASS | Warm, personal, first-person voice per brand-voice.md; no politics; no AI-slop phrasing in any draft. |
| Platform-native structure and format requirements met | PASS | Pulled from linkedin-review.md, instagram-review.md, facebook-review.md — all three PASS with no open revisions. |
| Hook strength and readability | PASS | Each platform has its own hook, correctly sized to that platform's truncation point (LinkedIn ~210, Instagram ~125, Facebook clear-but-looser). |
| Image relevant, original, consistent with style guide, correctly sized | **NEEDS HUMAN DECISION** | Per run instructions, the room-mockup photo (`chosen_images.mockup_url`, catalog index 1 — teal wall, plant, warm light) is a real product photo, not a style-guide-generated image, which is correct per this run's explicit instruction to use the mockup over Gemini generation. However, it could **not** be downloaded or cropped to platform dimensions this run (egress to images.squarespace-cdn.com returned "403 Forbidden" on the one attempt made, not retried per instructions) — so it is passed to Buffer uncropped, at its native aspect ratio, not LinkedIn's 1200x627 / Instagram's 1080x1350 / Facebook's 1200x630. A human should confirm it displays acceptably in Buffer's composer per platform, or crop it locally before scheduling. |
| Alt text accurate, matches final image and post | **NEEDS HUMAN DECISION** | Alt text (alt-text/linkedin.md, instagram.md, facebook.md) is based on the catalog's product description plus a prior human/Claude viewing note recorded 2026-09-01 ("teal wall, plant, warm light... AVOID idx 6/7"), not a fresh visual check this run (same egress block as above). Confidence is reasonably high since that prior note reflects an actual human/Claude viewing, but a human should do a final visual confirmation against the live image before publishing. |
| Tags/mentions appropriate, minimal, not forced, no unwanted third-party tagging | PASS | LinkedIn: none (appropriate for this post). Instagram: exactly 5, real mix. Facebook: 1 (#WholeheartedArts). No third parties tagged. |
| Compliance constraints from client profile respected | PASS | No professional/medical/legal claims; no politics; no fabricated AI-automation claims (topic doesn't touch that pillar at all). |
| No secrets/API keys/private info anywhere in the package | PASS | Reviewed all files in this topic folder — no keys, tokens, or private info present. |

## Summary of NEEDS HUMAN DECISION items (do not bury)

1. **Image not downloaded/cropped this run** — egress to
   images.squarespace-cdn.com is blocked in this sandbox (403 Forbidden,
   one attempt, not retried per instructions). The raw `mockup_url` was
   passed straight to Buffer for all three platforms; Buffer's own
   servers will fetch it independently. Confirm it displays correctly in
   Buffer's composer, or crop it locally to platform dimensions before
   scheduling.
2. **Alt text not visually re-verified this run** — written from the
   catalog description and a prior (2026-09-01) human/Claude viewing
   note rather than a fresh look at the image. Reasonably reliable, but
   a human should do a final visual check before publishing.

No FAIL items. Package is **review-ready** across all three platforms,
with the two items above flagged for human attention (not blockers to
staging in Buffer per the run's explicit instructions, but blockers to
final approval/scheduling).
