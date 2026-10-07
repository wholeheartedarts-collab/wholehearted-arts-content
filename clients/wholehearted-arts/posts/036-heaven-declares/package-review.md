# Content Package Review: "Heaven Declares" (LinkedIn + Instagram)

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal clear and match brief | PASS | Art-collectors pillar; "worship is where fragments get offered" takeaway; matches research.md's chosen angle. |
| Every factual claim/statistic/example supported | PASS | Pulled from fact-check.md — no UNSUPPORTED claims in either draft. |
| Balanced treatment where topic has real risks/drawbacks | N/A | Faith/art reflection topic has no material risk-balance requirement (unlike the AI-automation pillar); research.md's "Risks/limitations" section (Psalm 19 overlap, availability drift) was handled at the selection/drafting stage, not something the post itself needs to caveat. |
| No fabricated facts, quotations, personal experiences, or results | PASS | All quotations verified (fact-check.md); no invented anecdote — first-person process language restates the artist's own published description. |
| Client voice and avoid-list rules followed (no politics; no AI-slop) | PASS | Both platform reviews confirm voice fit; no politics anywhere. The politically-adjacent alternative painting ("Let Our Light Continue to Shine," an explicit Israel/Hanukkah prayer) was excluded at selection — see research.md. |
| Platform-native structure/current format requirements met | PASS | Confirmed via linkedin-review.md and instagram-review.md, both PASS on first draft. |
| Hook strength and readability | PASS | Both hooks are specific, grounded, and platform-length-appropriate. |
| Image relevant, original, consistent with style-guide, correctly sized | **NEEDS HUMAN DECISION** | Using the catalog's pre-verified `chosen_images.mockup_url` (real product photo, not a generated image — this is the "real photo" path, not a style-guide/Gemini image). Relevant and originally-sourced, yes. **Not cropped to platform dimensions** (LinkedIn 1200x627 / Instagram 1080x1350) — egress to images.squarespace-cdn.com failed in this sandbox (tested once via curl, not retried per run instructions), so the uncropped source URL is passed directly to Buffer, which will fetch it independently. A human should check how it renders on each platform and crop/replace if needed. |
| Alt text accurate, matches final image and post | **NEEDS HUMAN DECISION** | Alt text (alt-text/linkedin.md, alt-text/instagram.md) is built from the catalog entry's description and the `chosen_images.note` (confirms a white-brick/bright-daylight room mockup), not from direct visual inspection — the image could not be downloaded this session. A human should visually confirm the alt text matches the actual photo once viewable. |
| Tags/mentions appropriate, minimal, no unwanted third-party tagging | PASS | LinkedIn: one relevant tag. Instagram: five relevant tags, no more. No third parties tagged. |
| Compliance constraints from client profile respected | PASS | No professional/medical/legal claims; no CTA conflicts (soft CTA default used, consistent with "no approved CTAs yet"). |
| No secrets/API keys/private info in output package | PASS | Checked all files in this topic folder — none present. |

## Overlap-with-post-004 note (resolved, not an open decision)

Both "Heaven Declares" and post 004 ("Psalm of the Birch Forest") cite Psalm 19, per the catalog's caution_note. This draft deliberately uses Psalm 19:7-10/14 (God's Word) and 2 Corinthians 4:7, not Psalm 19:1-4 (creation's silent witness, 004's angle) — see research.md's "Differentiation from post 004" section. Flagging here for visibility, not as an open decision; both platform reviews passed on this basis.

## Summary of NEEDS HUMAN DECISION items (do not bury)

1. **Instagram's Buffer channel is disconnected** (`isDisconnected: true`, confirmed via `list_channels` and `get_channel` on 2026-10-07) — no Instagram draft could be staged in Buffer this run. LinkedIn staged successfully (channel connected). Instagram's finished post text, image URL, and alt text are ready in this folder; Agata needs to either reconnect the Instagram channel in Buffer (Settings → Channels) so a future run can stage it, or post it manually in the meantime.
2. **Image not downloaded/cropped to platform dimensions** — uncropped source URL passed to Buffer/used for the manual-path Instagram text; sandbox egress to the image CDN is blocked.
3. **Alt text not visually verified** — written from the catalog description and `chosen_images.note`, not a direct look at the photo.

Nothing else is outstanding. No FAILs.
