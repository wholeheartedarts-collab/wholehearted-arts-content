# Content Package Review — 026 Awakened Fields

Covers all three platform variants (LinkedIn, Instagram, Facebook)
together, per CLAUDE.md's multi-platform package-review convention.

| Check | Verdict | Notes |
|---|---|---|
| Topic, audience, takeaway, tone, goal clear and match brief | PASS | Art-collectors audience, faith/emotion pillar, thin-narrative image-led post per research.md's recommendation. Consistent across all 3 drafts. |
| Every factual claim/statistic/example supported | PASS | See fact-check.md — no UNSUPPORTED claims; one phrasing softened before this review to remove an invented personal-anecdote flourish, now consistent with post 025's established safe pattern for editorial scripture pairings. |
| Balanced treatment of real risks/drawbacks | N/A | Not a claims-heavy or risk-bearing topic (single art piece, no automation/business claims). |
| No fabricated facts, quotations, personal experiences, or results | PASS | Psalm 65 pairing explicitly disclosed in every draft as the writer's own association, not Agata's stated inspiration — no invented anecdote remains after the fact-check revision. |
| Client voice / avoid-list (no politics, no AI-slop) | PASS | First-person, warm, sensory language per brand-voice.md; no political content; no hype phrasing. |
| Platform-native structure per platform review | PASS | See linkedin-review.md, instagram-review.md, facebook-review.md — all PASS, no open revisions. |
| Hook strength and readability | PASS | Each platform has its own hook length/tone, not a copy-pasted single hook. |
| Image relevant, original, consistent with style-guide.json, correctly sized | **NEEDS HUMAN DECISION** | Per run instructions, a real product-listing room mockup (`chosen_images.mockup_url`, catalog index 0 — human-verified 2026-09-01 as a genuine living-room mockup, not a flat shot) is used instead of a generated image, which is the correct call per the human-directed real-photo path. However, the image could **not be downloaded and cropped** to each platform's dimensions this run (egress to images.squarespace-cdn.com blocked, not retried per run instructions) — the same raw, uncropped source URL was passed to Buffer for all three platforms. A human should confirm it displays acceptably in each platform's aspect ratio, or crop it locally before scheduling. |
| Alt text accurate and matches final image/post | **NEEDS HUMAN DECISION** | Alt text (per platform, in `alt-text/`) was written from the catalog's description and the `chosen_images.note`, not from direct visual inspection, since the image could not be downloaded this run. A human should confirm it actually matches the image before publishing. |
| Tags/mentions appropriate, minimal, no unwanted third-party tagging | PASS | LinkedIn: none. Instagram: 5, capped, relevant mix. Facebook: 1 (#wholeheartedarts). No third parties tagged. |
| Compliance constraints from client profile respected | PASS | No professional/medical/legal claims; price not stated (avoids any need to verify a moving price point); no politics. |
| No secrets, API keys, or private information in output | PASS | Checked all files in this topic folder — no keys, tokens, or private data present. |

## Summary of NEEDS HUMAN DECISION items (do not bury)

1. **Image not downloaded/cropped this run** — the raw mockup URL (not
   platform-sized) was passed straight to Buffer for LinkedIn, Instagram,
   and Facebook. Confirm it reads correctly in Buffer's composer per
   platform, or crop it locally (LinkedIn 1200x627, Instagram 1080x1350,
   Facebook 1200x630) before scheduling.
2. **Alt text not visually verified** — written from the catalog's
   description and `chosen_images.note` only, since the image couldn't be
   downloaded. Please confirm it matches the actual photo.

Both stem from the same root cause: sandbox egress to
`images.squarespace-cdn.com` returned `403 Forbidden` and was not
retried, per this run's explicit instructions. Everything else in the
package — research, all three post drafts, platform reviews, and fact-
check — passed cleanly with no open issues.

## Result

**PASS with 2 NEEDS HUMAN DECISION items** (both image-related, both
disclosed above). No FAILs. Package proceeds to `status.json` at
review-ready and Buffer staging per publishing-handoff's Critical Buffer
limitation section.
