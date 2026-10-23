# Content Package Review — 043 "A Field Full of Yes" (LinkedIn + Instagram)

## NEEDS HUMAN DECISION items (summary — see detail below)

1. **Atelier Collection has no remaining viable unused entry.** After
   reconciling the catalog's stale used/unused tracking against the
   actual post folders (001-042), every Atelier Collection painting has
   now been used in a post except one: "Let Our Light Continue to
   Shine," whose own description is an explicit prayer for peace in
   Israel/the Jewish people. Per this client's no-politics avoid-list,
   this run judged that piece unsuitable for unattended automated
   selection (same call made by the 042 run) and selected from the
   Studio Collection instead, even though the deterministic rule's raw
   used-count comparison pointed to Atelier (17 used vs. Studio's 23
   after reconciliation, both counts higher than the catalog's own
   stale 7/7). **A human should decide**: (a) whether to have a human
   write "Let Our Light Continue to Shine" directly (outside this
   pipeline) with careful framing, (b) regenerate/expand the Atelier
   Collection catalog if more pieces exist that aren't showing, or (c)
   accept that Atelier selections are paused until one of the above
   happens — future automated runs will keep falling back to Studio
   otherwise.
2. **No photo-mockup exists for "A Field Full of Yes."** The catalog has
   no `chosen_images` entry for this painting, so no human has reviewed
   its photos to pick a styled room-mockup shot. Both platforms use the
   flat/primary product photo instead. A human could add a
   `chosen_images` selection for this piece later if a mockup photo
   exists among its listing images.
3. **Image could not be downloaded, cropped, or visually verified** —
   confirmed 403 on a single direct test fetch to the Squarespace CDN
   (sandbox egress policy), per the "test once, don't retry" rule. The
   raw image URL was passed straight to Buffer (which fetches
   independently of this sandbox) for both platforms, uncropped to
   platform dimensions. Alt text was written from the catalog's text
   description only, not from visual inspection, and is explicitly
   flagged as such in both alt-text files.

## Checklist

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal clear and matches brief | PASS | Art-collector audience, faith/overcoming pillar, soft reflective tone matching brand-voice.md. |
| Every factual claim supported ([[factual-verification]]) | PASS | See fact-check.md — all claims SOURCED; one fabrication risk caught and removed during drafting, not merely softened. |
| Balanced treatment where real risks/drawbacks exist | N/A | Not a topic with counterarguments (art piece), no one-sidedness concern. |
| No fabricated facts/quotes/personal experiences | PASS | Confirmed after revision — see fact-check.md note on the removed invented backstory/confession. |
| Client voice and avoid-list rules followed | PASS | No politics; no AI-slop phrasing; voice checked against brand-voice.md in both platform reviews. |
| Platform-native structure/current requirements met | PASS | See linkedin-review.md and instagram-review.md, both PASS on all items. |
| Hook strength and readability | PASS | Both hooks stand alone within their platform's truncation window and are specific to this piece, not generic. |
| Image relevant, original, consistent with style-guide, correctly sized | NEEDS HUMAN DECISION | Relevant and accurate (flat catalog photo of the actual painting), but not locally cropped to style-guide dimensions due to confirmed egress block (sandbox limitation, not a content problem) — see item 3 above. Not a copied "reference" image in the prohibited sense; it is the client's own real product photo of her own painting. |
| Alt text accurate, matches final image and post | NEEDS HUMAN DECISION | Written from text description only, not visual inspection — flagged explicitly in both alt-text files per item 3 above. |
| Tags/mentions appropriate, minimal, no unwanted third-party tagging | PASS | LinkedIn: none used (correctly judged unnecessary). Instagram: exactly 5, all directly relevant to this piece. |
| Compliance constraints from client profile respected | PASS | No professional/medical/legal claims; no AI-automation claims involved (this topic is pure art pillar). |
| No secrets/API keys/private information in output | PASS | Verified — no keys or secrets in any file produced. |

## Result

No FAIL items. Three NEEDS HUMAN DECISION items recorded above (Atelier
exhaustion, no mockup selected, image not visually verified/cropped) —
all carried forward prominently into the Step 13 email and final run
summary. Package is presented as review-ready for both platforms.
