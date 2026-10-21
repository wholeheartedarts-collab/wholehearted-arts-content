# Content Package Review — 042 Breaking the Chains (LinkedIn + Instagram)

## NEEDS HUMAN DECISION items (summary — see details below)

1. **Collection-selection fallback**: the deterministic selection rule
   pointed to the Atelier Collection this run (fewer used entries, 17 vs
   22), but Atelier's only remaining unused entry, "Let Our Light
   Continue to Shine," is a mixed-media piece whose own description
   states it is "my heartfelt prayer for peace in #Israel and for all
   Jewish people worldwide" — geopolitically sensitive subject matter
   that this run judged unsuitable for unattended selection under the
   client's explicit no-politics avoid-list, even though the catalog
   does not carry a `caution_note` field on it. The run fell back to the
   Studio Collection instead and picked "Breaking the Chains." A human
   should confirm this judgment call, and/or decide whether to formally
   tag that Atelier entry with a `caution_note` in the catalog so future
   runs don't have to re-derive this.
2. **No image could be downloaded or visually verified**: this
   sandbox's egress to the Squarespace image CDN is blocked (confirmed
   by a failed test fetch, 403 Forbidden). The catalog's flat
   `primary_image_url` was passed through to Buffer uncropped and
   unverified — alt text is based on catalog text data only, not an
   actual look at the image. A human should open the Buffer drafts and
   confirm the image looks right before queuing.
3. **No `chosen_images` mockup exists** for "Breaking the Chains" — per
   the routine's instructions, the flat product photo was used instead
   of a styled room mockup, and this is stated plainly rather than
   claiming a room scene. A human may want to add a mockup selection to
   the catalog for this painting for future reuse.

## Checklist

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal clear | PASS | Art-collector audience, faith/overcoming-struggle pillar, reflective tone matching thin source material. |
| Every factual claim supported | PASS | See `fact-check.md` — no UNSUPPORTED claims. |
| Balanced treatment where topic has real risks/drawbacks | N/A | Not a topic with counterarguments (visual-art reflection, not a claims-heavy topic). |
| No fabricated facts/quotations/personal experiences | PASS | Confirmed — post explicitly states no specific story/verse was in mind, matching the real thin catalog description. |
| Client voice and avoid-list rules followed | PASS | No politics; no AI-slop phrasing; matches brand-voice.md register. |
| Platform-native structure (LinkedIn) | PASS | See `linkedin-review.md`. |
| Platform-native structure (Instagram) | PASS | See `instagram-review.md`, hashtags capped at 5. |
| Hook strength and readability (both platforms) | PASS | See platform reviews. |
| Image relevant, original, style-guide-consistent, correctly sized | NEEDS HUMAN DECISION | Real catalog photo (not generated) per this routine's instructions for using actual product photos; could not be downloaded/cropped to platform dimensions or visually verified due to blocked egress — see item 2 above. Not a generated image, so style-guide.json's generation-specific rules (palette/mood/prohibited) don't strictly apply, but its `dimensions` map targets (1200x627 LinkedIn, 1080x1350 Instagram) were not achieved. |
| Alt text accurate and matches final image/post | NEEDS HUMAN DECISION | Alt text is honest about not being visually verified (see item 2); accurate to the extent the catalog text data allows. |
| Tags/mentions appropriate, minimal, no unwanted third-party tagging | PASS | LinkedIn: none. Instagram: 5 relevant tags, no third parties tagged. |
| Compliance constraints from profile respected | PASS | No professional/medical/legal claims; pricing/availability stated accurately (1 in stock), not overstated. |
| No secrets/API keys/private info in output | PASS | Confirmed by review of all files in this topic folder. |

## Overall verdict

**PASS, with 3 NEEDS HUMAN DECISION items flagged above.** The package
is presented as review-ready; nothing is approved, scheduled, or
published by this run.
