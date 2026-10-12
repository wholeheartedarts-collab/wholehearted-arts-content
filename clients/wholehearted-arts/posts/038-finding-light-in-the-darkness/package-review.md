# Package Review — 038 "Finding Light in the Darkness # 2"

Covers both platform variants (LinkedIn, Instagram). Facebook not
produced — Instagram cross-posts to the Facebook Page per current
client scope (2026-09-30 change).

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal clear, matches brief | PASS | Art-collector pillar; faith/emotion/healing/overcoming-struggle angle; matches brief.md. |
| Every factual claim supported | PASS | Pulled from fact-check.md — no UNSUPPORTED claims. |
| Balanced treatment of real risks/drawbacks | N/A | Not an applicable check for this topic (no claims of adoption stats, business results, or one-sided argument — this is the AI-automation pillar's requirement, not the art pillar's). |
| No fabricated facts/quotes/personal experiences | PASS | No invented backstory beyond the catalog listing; scripture paraphrased, not misattributed. |
| Client voice / avoid-list (no politics, no AI-slop) | PASS | Confirmed in both platform reviews. |
| Platform-native structure (LinkedIn) | PASS | Per linkedin-review.md. |
| Platform-native structure (Instagram) | PASS | Per instagram-review.md, hashtags at cap of 5. |
| Hook strength and readability (both) | PASS | Distinct hooks per platform, neither reused verbatim. |
| Image relevant to finished post | PASS | Real product photo of the actual painting discussed — directly relevant, not generic/stock. |
| Image original (not a copied reference) | PASS | This is Agata's own artwork photo from her live product listing, not a third-party or AI-generated image. |
| Image consistent with style-guide.json | NEEDS HUMAN DECISION | This run uses a real catalog photo per CLAUDE.md's "real/sourced image" path, not a Gemini-generated image, so the placeholder style-guide's generation prompts don't apply. More importantly: **no `chosen_images` mockup selection exists for this painting** — a human has not reviewed its 11 product photos to confirm a room mockup. This run used `primary_image_url` (flat shot) only, per the run's explicit fallback rule. Recommend a human (or a future session that can view images) sets `chosen_images` for this entry in painting-catalog.json. |
| Image correctly sized per platform | NEEDS HUMAN DECISION | Egress to the image CDN is blocked in this sandbox (confirmed: single curl attempt returned a proxy 403/tunnel failure, not retried per run instructions). No local LinkedIn 1200x627 / Instagram 1080x1350 crop could be produced. The same `primary_image_url` was passed straight to Buffer for both platforms uncropped — Buffer's own servers will fetch it independently. Not a FAIL per the run's explicit egress-fallback rule, but sizing/letterboxing was not done and should be reviewed once egress or local tooling allows it. |
| Alt text accurate, matches final image/post | NEEDS HUMAN DECISION | Alt text (alt-text/linkedin.md, alt-text/instagram.md) is based on the catalog's written description only — the image itself was never visually verified (same egress block). Flagged explicitly rather than guessing visual details. |
| Tags/mentions appropriate, minimal, no third-party tagging | PASS | LinkedIn: none (stated rationale). Instagram: 5, all topic-relevant, no third parties tagged. |
| Compliance constraints from client profile respected | PASS | No professional/medical/legal claims; no political content. |
| No secrets/API keys/private info in output | PASS | No keys or credentials written anywhere in this package. |

## Summary verdict

**No FAILs.** Package was staged as Buffer drafts (review-ready), with
four NEEDS HUMAN DECISION items carried forward:

1. **Instagram channel is disconnected in Buffer** (`isDisconnected:
   true`, confirmed via `list_channels` and `get_channel` on
   2026-10-12). The draft was still created and `get_post` confirms it
   is genuinely inert (status draft, dueAt/sentAt null, sharedNow
   false), but Agata will not be able to "Add to Queue" or "Share Now"
   from it until she reconnects the Instagram account in Buffer's
   channel settings. This is the most important item in this run — the
   LinkedIn draft is fully usable today; the Instagram draft is parked
   and waiting on a reconnect.
2. No room-mockup image was available/selected for this painting —
   flat product photo used instead, correctly not described as a room
   scene anywhere in the package.
3. The image could not be downloaded/cropped per-platform in this
   sandbox (image-CDN egress blocked) — passed through to Buffer as a
   raw URL instead, which Buffer's own servers fetched independently.
4. Alt text for both platforms is based on written product description
   only, not on a human/AI visual check of the actual photo.

None of these are reasons to block staging as drafts — they're reasons
a human should look at the Buffer drafts before approving/scheduling,
which this run does not do regardless.
