# Content package review — Post 055 "Seeking His Will"

Covers the LinkedIn + Instagram package together (no Facebook variant —
Instagram cross-posts to the Facebook Page per 2026-09-30 decision).

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal clear and match brief | PASS | Faith/art-collector pillar, trusting God's timing, consistent across both drafts. |
| Every factual claim supported | PASS | See fact-check.md — no UNSUPPORTED items. |
| Balanced treatment where topic has real risks | N/A | Not a topic with drawbacks/limitations to balance (not the AI-automation pillar). |
| No fabricated facts/quotes/personal experiences | PASS | No invented backstory; thin-narrative piece kept shorter and image-led per skip_rules. |
| Client voice / avoid-list followed | PASS | No politics; no AI-slop phrasing; voice matches brand-voice.md. |
| Platform-native structure (LinkedIn) | PASS | See linkedin-review.md — full PASS. |
| Platform-native structure (Instagram) | PASS | See instagram-review.md — full PASS, hashtags at cap of 5. |
| Hook strength and readability | PASS | Both hooks grounded in the documented scripture-in-paint fact. |
| Image relevant, original, consistent with style guide, correctly sized | **NEEDS HUMAN DECISION** | No `chosen_images` mockup exists for this catalog entry — used `primary_image_url` (flat product photo) for both platforms, unconfirmed as to whether it shows a styled scene. Also not locally cropped to platform dimensions (LinkedIn 1200x627 / Instagram 1080x1350) — sandbox egress to the Squarespace CDN failed (CONNECT tunnel 403, tested once per policy, not retried), so the raw URL is passed straight to Buffer, which will fetch it independently. A human should confirm the image reads correctly once staged in Buffer and decide whether a mockup photo should be selected for this painting going forward. |
| Alt text accurate, matches final image/post | **NEEDS HUMAN DECISION** | Alt text (alt-text/linkedin.md, alt-text/instagram.md) was written from the catalog's text description only, since the image was never visually verified in this sandbox. Accurate to the documented facts, but should be double-checked by a human against the actual photo. |
| Tags/mentions appropriate, minimal, no unwanted third-party tagging | PASS | LinkedIn: none used (by design). Instagram: 5 tags, all topic-relevant, no third parties. |
| Compliance constraints from client profile respected | PASS | No professional/medical/legal claims; price/availability flags observed (no price stated, no purchase claim, given sold-out snapshot). |
| No secrets/API keys/private info in output | PASS | Checked both drafts, research files, and this review — none present. |

## NEEDS HUMAN DECISION items (carried to Step 13 email and run summary)

1. **No `chosen_images` mockup for "Seeking His Will."** Used the flat
   product photo (`primary_image_url`) for both LinkedIn and Instagram.
   Not confirmed whether a room-mockup photo exists among this listing's
   other images that a human should select instead.
2. **Image not locally downloaded/cropped.** Sandbox egress to
   `images.squarespace-cdn.com` failed (403), so neither platform crop
   was produced locally; the raw URL was passed to Buffer, which fetches
   independently. Alt text is based on the catalog's text description
   only and has not been visually verified.
3. **Standing Atelier-exhaustion decision (carried forward, 18
   consecutive runs, posts 039-055).** Atelier's only remaining
   non-flagged, non-sold unused entry, "Let Our Light Continue to
   Shine," continues to be excluded as politically-adjacent (explicit
   prayer for peace in Israel/the Jewish people), forcing every recent
   run including this one onto Studio. This needs an explicit decision
   from Agata — confirm the exclusion stands long-term, or direct a
   specific, human-reviewed treatment of that piece — rather than
   another automated fallback.
4. **Price/availability on "Seeking His Will."** Catalog snapshot shows
   this exact piece as sold out (0 in stock) and on sale at the
   snapshot. Neither draft states a price or claims it's purchasable;
   if Agata has since relisted or restocked it, she can add pricing/CTA
   herself before scheduling.

## Hard-rule check

No FAIL items. Package is **review-ready** for both platforms, with the
four items above surfaced explicitly rather than guessed at or buried.
