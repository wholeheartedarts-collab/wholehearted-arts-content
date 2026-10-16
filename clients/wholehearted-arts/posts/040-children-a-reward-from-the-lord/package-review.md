# Package Review — 040 "Children — Reward from the LORD"

Covers both platform variants (LinkedIn, Instagram). Facebook not
produced — Instagram cross-posts to the Facebook Page per current
client scope (2026-09-30 change).

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal clear, matches brief | PASS | Art-collector pillar; faith/prayer and family content pillars; matches research.md's executive summary. |
| Every factual claim supported | PASS | Pulled from fact-check.md — no UNSUPPORTED claims. |
| Balanced treatment of real risks/drawbacks | N/A | Not an applicable check for this topic (art/scripture reflection, not a stats- or claims-driven topic — that requirement is for the AI-automation pillar). |
| No fabricated facts/quotes/personal experiences | PASS | No invented backstory beyond the catalog's own subject line and scripture text; Psalm 127 quoted verbatim and independently verified, not paraphrased or misattributed. |
| Client voice / avoid-list (no politics, no AI-slop) | PASS | Confirmed in both platform reviews. Scripture framing stays on the passage's actual point (dependence on God), not prescriptive commentary. |
| Platform-native structure (LinkedIn) | PASS | Per linkedin-review.md. |
| Platform-native structure (Instagram) | PASS | Per instagram-review.md, hashtags at cap of 5. |
| Hook strength and readability (both) | PASS | Distinct hooks per platform (LinkedIn ~140 chars, Instagram ~87 chars), neither reused verbatim. |
| Image relevant to finished post | PASS | Real product photo of the actual painting discussed (the praying-parents scene with scripture written on canvas) — directly relevant, not generic/stock. |
| Image original (not a copied reference) | PASS | Agata's own artwork photo from her live product listing, not a third-party or AI-generated image. |
| Image consistent with style-guide.json | NEEDS HUMAN DECISION | Real catalog photo used per the run's sourced-image path, not Gemini generation, so the placeholder style guide's generation prompts don't apply. **No `chosen_images` mockup selection exists for this painting** — no human/Claude has reviewed its 6 product photos to pick a room mockup. `primary_image_url` (flat shot, index 0, square) was used for both platforms per the explicit fallback rule. Recommend a human (or a future session that can view images) sets `chosen_images` for this entry in painting-catalog.json. |
| Image correctly sized per platform | NEEDS HUMAN DECISION | Egress to the image CDN (images.squarespace-cdn.com) was blocked in this sandbox — confirmed via a single `curl` attempt (`CONNECT tunnel failed, 403`), not retried per run instructions. No local LinkedIn 1200x627 / Instagram 1080x1350 crop was produced. The same `primary_image_url` was passed straight to Buffer for both platforms uncropped; Buffer's own servers fetch it independently. Not a FAIL per the run's explicit egress-fallback rule, but sizing/letterboxing should be reviewed once egress or local tooling allows it. |
| Alt text accurate, matches final image/post | NEEDS HUMAN DECISION | `alt-text/linkedin.md` and `alt-text/instagram.md` are based on the catalog's written subject description, materials, and scripture text only — the image itself was never visually verified (same egress block). `alt_from_site` was null in the catalog. Flagged explicitly in both files rather than guessing visual details. |
| Tags/mentions appropriate, minimal, no third-party tagging | PASS | LinkedIn: none, with stated rationale. Instagram: exactly 5, all topic-relevant, no third parties tagged. |
| Compliance constraints from client profile respected | PASS | No professional/medical/legal claims; no political content. |
| No secrets/API keys/private info in output | PASS | No keys or credentials written anywhere in this package. |

## Selection-process finding carried forward

**Atelier Collection's catalog "unused" list is stale for a second
consecutive run.** All 10 of its non-flagged "unused" entries (Awakened
Fields, Gathered Light, Guardian of Innocence, Heaven Declares, Love
Eternal Rhapsody, Messenger, Never Stop Wonder, Patience, The Strength of
Three Strands, Whimsical Gdansk) are already used in prior posts; the
only true "unused" Atelier entry ("Let Our Light Continue to Shine") is
the same Israel/Hanukkah-themed, zero-stock piece flagged as a
NEEDS-HUMAN-DECISION borderline-politics concern on post 039. This run
again treated Atelier as having no safely selectable entry and drew from
Studio instead, consistent with that precedent — flagged here, and in the
Step 13 email, for a human to regenerate/re-curate the Atelier
`unused` list in painting-catalog.json so future runs aren't repeatedly
blocked on the same two items.

## Buffer staging finding

**Instagram channel remains disconnected in Buffer** (`isDisconnected:
true`, confirmed via `list_channels` on 2026-10-16) — the same recurring
issue flagged on posts 036-039. Following the precedent set on posts
038/039, `create_post` was attempted for Instagram anyway; it succeeded
and `get_post` confirms the draft is genuinely inert (status draft,
dueAt/sentAt null, sharedNow false, schedulingType automatic). The
LinkedIn draft is fully usable today; the Instagram draft exists but
Agata will not be able to "Add to Queue" or "Share Now" from it until
she reconnects the Instagram account in Buffer's channel settings.

## Summary verdict

**No FAILs.** Package is review-ready for both platforms, with four
NEEDS HUMAN DECISION items carried forward (image mockup curation, image
sizing/cropping, alt-text visual verification, Instagram channel
reconnect), plus the recurring Atelier-catalog-staleness finding above.
None of these block staging as inert Buffer drafts, which this run does;
none of them are approved, scheduled, or published by this run.
