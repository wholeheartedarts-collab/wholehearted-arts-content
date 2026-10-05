# Content package review — 035 "Where Grace Settles" (LinkedIn + Instagram)

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal clear and match brief | PASS | Art/faith pillar, art-collector audience, "grace meets you unfinished" takeaway, reflective warm tone — consistent across both drafts. |
| Every factual claim supported (pulled from fact-check.md) | PASS | See fact-check.md — one UNSUPPORTED claim (unconfirmed studio anecdote) was caught and rewritten before this gate; fact-check.md records final PASS. |
| Balanced treatment of real risks/drawbacks | PASS (N/A) | Not a topic with inherent risk/drawback dimension (not the AI-automation pillar) — research.md's "Risks/limitations" section (thin narrative, price discrepancy, unconfirmed mockup) is about pipeline data quality, not the content's claims, and is handled below and in the email, not as a post-body balance issue. |
| No fabricated facts/quotations/personal experiences/results | PASS | Fixed during fact-check (see fact-check.md) — current drafts contain no invented anecdote. Philippians 1:6 quoted verbatim and verified. |
| Client voice and avoid-list rules followed | PASS | No politics; no AI-slop phrasing; matches brand-voice.md's do/avoid lists (first-person, sensory, non-preachy faith references). |
| Platform-native structure (LinkedIn format requirements) | PASS | Pulled from linkedin-review.md — PASS on all items. |
| Platform-native structure (Instagram format requirements) | PASS | Pulled from instagram-review.md — PASS on all items, hashtags exactly 5 (cap respected). |
| Hook strength and readability | PASS | Both hooks stand alone within their platform's truncation point; grounded in the research angle. |
| Image relevant, original, consistent with style-guide.json, correctly sized | **NEEDS HUMAN DECISION** | Image is the painting's own real product photo (`primary_image_url`, index 0) — relevant and not a copied "reference" in the AI-generation sense, so no conflict with style-guide prohibitions. However: (1) this entry has no `chosen_images` selection, so no one has visually confirmed this photo is the best choice among the 5 available, or whether a better room-mockup photo exists among the other 4 indexes; (2) the image was not downloaded or cropped to each platform's exact dimensions (LinkedIn 1200x627 / Instagram 1080x1350) — egress to images.squarespace-cdn.com is blocked in this sandbox, so the uncropped source URL is being passed straight to Buffer, which will fetch and display it at its native aspect ratio instead of the style guide's target crop. Both are real open items for Agata, not fabrication risks. |
| Alt text accurate and matches final image/post | **NEEDS HUMAN DECISION** | Alt text (alt-text/linkedin.md, alt-text/instagram.md) is written from the catalog's description text only, since the image was never visually inspected (by a human or by Claude) — it explicitly flags this. Accurate as far as it goes, but not independently verified against the actual photo. |
| Tags/mentions appropriate, minimal, no unwanted third-party tagging | PASS | LinkedIn: none (reasoned). Instagram: exactly 5, relevant mix, no third-party tags. |
| Compliance constraints from client profile respected | PASS | No professional/medical/legal claims; no fabricated client results; soft CTA default used (no approved CTA list yet). |
| No secrets/API keys/private information in output | PASS | Checked all files in this topic folder — none present. |

## Summary verdict: PASS, with two NEEDS HUMAN DECISION items (both listed above and repeated in the Step 13 email)

1. **No confirmed mockup image** — this painting's catalog entry has no `chosen_images` field, so no human/Claude session has reviewed its 5 product photos to pick the best one (room mockup vs. flat shot). `primary_image_url` (index 0) was used by default. A human should view the listing's photos and set `chosen_images` for this entry if a better one exists.
2. **Image not cropped to platform dimensions** — egress to the image CDN is blocked in this sandbox, so the source photo was passed to Buffer uncropped rather than resized to the style guide's 1200x627 (LinkedIn) / 1080x1350 (Instagram) targets. Buffer will display it at its native aspect ratio. Not a content-accuracy issue, but a presentation one worth knowing about.

Additionally carried forward from research.md (not NEEDS HUMAN DECISION items for the post content itself, since neither post states a price, but worth Agata's attention): the catalog's price field for this painting ($475) disagrees with the price written inside its own description text ($675) — a data-entry issue on the website/catalog, not something this post needed to resolve.
