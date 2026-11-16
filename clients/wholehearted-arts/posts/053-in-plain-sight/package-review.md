# Content Package Review — Topic 053 "In Plain Sight"

Covers both platform variants (LinkedIn + Instagram). No Facebook
variant — Instagram cross-posts to the Facebook Page as of 2026-09-30.

## NEEDS HUMAN DECISION items (read first)

1. **Atelier Collection has zero viable candidates for the 15th
   consecutive run (posts 039-053).** The selection rule points to
   Atelier this run (reconciled usage: Atelier 18, Studio 34), but all
   18 Atelier catalog entries are now either already used or flagged.
   The sole remaining Atelier entry, "Let Our Light Continue to Shine,"
   is an explicit prayer for peace in Israel/the Jewish people woven
   into Hanukkah blessings — carried forward as politically-adjacent,
   unresolved. Agata needs to either explicitly clear this piece for
   use, or have the Atelier side of the catalog refreshed with new
   inventory; until then every run will keep falling back to Studio.
2. **No `chosen_images` mockup for "In Plain Sight."** This entry has
   never had a human/Claude view its 11 product photos to pick a room
   mockup. `primary_image_url` (a flat product photo) was used for both
   platforms instead, per this run's instructions. Needs a human to
   view the listing and set `chosen_images` for future use.
3. **New finding this run: "Eyes of Fear - War"** (Studio, unused,
   in stock) was excluded as a candidate because its catalog
   description explicitly frames it around a "chaotic and violent
   backdrop" with war/conflict imagery — not caught by any
   `caution_note`, but judged too close to the no-politics-even-
   tangentially rule for an automated run to decide alone. Flagging for
   a human to confirm whether it's usable or should be formally
   caution-flagged in the catalog.
4. **Pricing is mid-sale and unverified** for the selected piece ($600
   list / $300 sale at snapshot). Neither draft quotes a price for this
   reason — if Agata wants to add a price in a comment reply, she
   should verify current pricing first.

## Checklist

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal clear and match brief | PASS | Art-collector audience, faith/healing pillar, reflective tone, clearly scoped to this run's instructions. |
| Every factual claim supported | PASS | Pulled from fact-check.md — no UNSUPPORTED claims in either draft. |
| Balanced treatment of real risks/limitations | N/A | Not a topic with inherent risk/drawback content (not the AI-automation pillar); limitations about thin source material and image verification are handled by omission (no invented backstory, no invented visual detail) rather than by a "risks" section in the post itself. |
| No fabricated facts/quotations/personal experiences/results | PASS | No invented backstory, no invented customer story, no claimed personal meaning attributed to Agata beyond the catalog's own series name. |
| Client voice and avoid-list rules followed | PASS | No politics; no AI-slop phrasing; checked against brand-voice.md. |
| Platform-native structure (LinkedIn) | PASS | Per linkedin-review.md — full PASS on all checklist items. |
| Platform-native structure (Instagram) | PASS | Per instagram-review.md — full PASS on all checklist items, hashtags at the 5-cap. |
| Hook strength and readability | PASS | Both hooks stand alone within their platform's truncation point. |
| Image relevant, original, style-guide-consistent, correctly sized | NEEDS HUMAN DECISION | Image is relevant (it is the actual painting) and original (real product photo, not AI-generated or copied reference), but it is an un-cropped flat product photo rather than a style-guide-sized crop or a room mockup — egress to the Squarespace CDN is blocked in this sandbox (confirmed, not retried), so no local crop could be produced. The public URL is passed to Buffer directly; Buffer's own servers will fetch it independently. See NEEDS HUMAN DECISION #2 above. |
| Alt text accurate, matches final image and post | PASS (with caveat) | Alt text is honest about not being visually verified and is based only on catalog text — accurate to what's actually known, not padded with invented visual detail. |
| Tags/mentions appropriate, minimal, no unwanted third-party tagging | PASS | LinkedIn: none. Instagram: 5 tags, all self-relevant, no third-party tags. |
| Compliance constraints from client profile respected | PASS | No professional/medical/legal claims; pricing deliberately omitted given unverified sale status. |
| No secrets/API keys/private information in output | PASS | Checked — no keys, no Agata personal contact info, nothing beyond public catalog data. |

## Status

`status.json` sets `linkedin` and `instagram` to `review-ready`,
`facebook` to `not-needed`. Nothing is approved, scheduled, or
published by this review.
