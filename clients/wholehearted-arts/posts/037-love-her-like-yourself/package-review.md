# Full Package Review — 037 "Love Her Like Yourself" (LinkedIn + Instagram)

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal clear and match brief | PASS | Marriage/faith angle on a specific Studio Collection piece; art-collectors audience; matches research.md. |
| Every factual claim supported | PASS | See fact-check.md — no UNSUPPORTED claims. |
| Balanced treatment of real risks/drawbacks | PASS | research.md's "Risks" section (preachiness, heteronormative reading) is reflected in both drafts by staying descriptive/specific rather than prescriptive or generalizing beyond the piece. |
| No fabricated facts/quotations/personal experiences | PASS | Only the catalog's own scripture text and product facts are used; no invented anecdote. |
| Client voice and avoid-list followed | PASS | No politics; no AI-slop phrasing; matches brand-voice.md per linkedin-review.md / instagram-review.md. |
| Platform-native structure (LinkedIn) | PASS | See linkedin-review.md. |
| Platform-native structure (Instagram, hashtags ≤5) | PASS | See instagram-review.md — exactly 5 tags. |
| Hook strength and readability | PASS | Both hooks are specific and curiosity-driving, grounded in the real scripture-on-canvas detail. |
| Image relevant, original, consistent with style-guide.json, correctly sized | **NEEDS HUMAN DECISION** | No `chosen_images.mockup_url` exists for this painting — `primary_image_url` (780x780 square, Squarespace's native crop) was used for both platforms rather than a human-verified mockup or a platform-correct crop. Egress to the image CDN is blocked in this sandbox, so the image was not downloaded or cropped to LinkedIn's 1200x627 or Instagram's 1080x1350 with Pillow. The same uncropped URL was passed to Buffer for both platforms. A human should pick a mockup image index (if the product listing has one worth using) and/or crop per platform. |
| Alt text accurate and matches final image/post | **NEEDS HUMAN DECISION** | Alt text was written from the catalog's text description only (not visually verified) and says so explicitly in both alt-text files. A human should confirm it against the actual photo. |
| Tags/mentions appropriate, minimal, not forced, no unwanted third-party tagging | PASS | 1 tag on LinkedIn, 5 on Instagram, all relevant to this piece; no one is tagged. |
| Compliance constraints from profile respected | PASS | No professional/medical/legal claims; no CTA beyond the approved soft-CTA default. |
| No secrets/API keys/private info in the package | PASS | Nothing of that kind appears anywhere in this topic's files. |

## NEEDS HUMAN DECISION items (both carried into Step 13 email and the final summary)

0. **Instagram channel disconnected in Buffer (recurring, unresolved since post 036 on 2026-10-07)** — `list_channels` shows the Instagram channel (`6a74f44c99afb44349156296`, @wholeheartedarts) as `isDisconnected: true`. Per publishing-handoff's staging rules, no `create_post` was attempted against it. Only the LinkedIn draft was staged in Buffer this run; Instagram's finished text/image/alt-text are ready in this folder for Agata to post manually, or to stage in Buffer herself once she reconnects the channel (Buffer → Settings → Channels → reconnect Instagram).
1. **No mockup image selected** — this painting has no `chosen_images` entry in the catalog. The flat product photo (`primary_image_url`, 780x780) was used for both LinkedIn and Instagram, not a styled room mockup. Agata may want to pick a mockup (if one exists among the product's other photos) and/or have this re-cropped per platform.
2. **Image not downloaded/cropped** — egress to the image CDN is blocked in this sandbox; the uncropped source URL was passed straight to Buffer for both platforms (Buffer's own servers will fetch it independently). Platform-correct cropping (1200x627 LinkedIn / 1080x1350 Instagram) has not happened.
3. **Alt text not visually verified** — written from the product description only; a human should confirm it matches the actual image.
4. **Price/availability staleness** — the catalog shows "Love Her Like Yourself" on sale ($300 from $350) with a note to verify before quoting; neither post quotes a price, but if Agata adds pricing herself before publishing, she should check the live listing first. The exhibition-pickup note in the catalog ("available... AFTER END of EXHIBITION at CHAMBERS WALK on SEPTEMBER 1ST") is already past as of this run but worth a quick confirmation that the piece has in fact shipped back / is available.

## Status

Both LinkedIn and Instagram text/voice/fact content: **PASS**, ready for `review-ready`.
Image and alt text: carried forward as **NEEDS HUMAN DECISION**, not a FAIL — the text and research are sound and the package is presented with these flagged, per the hard rule that NEEDS HUMAN DECISION items are surfaced, not silently resolved or hidden.
