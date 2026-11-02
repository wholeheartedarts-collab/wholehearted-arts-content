# Package Review — 047 "Where She Cried Flower Grew" (LinkedIn + Instagram)

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal clear | PASS | Art/faith pillar, art-collector audience, universal theme of grief transformed, matches brief. |
| Every factual claim supported | PASS | See fact-check.md — all claims SOURCED, none UNSUPPORTED. |
| Balanced treatment of real risks/drawbacks | PASS | Not a stats/advice topic with drawbacks to balance; research.md's "Risks/limitations" section (emotional weight, no specific-person claim, price volatility) is respected — both drafts stay general/universal, no price quoted. |
| No fabricated facts/quotes/personal experiences | PASS | Confirmed in fact-check.md. Painting's own words used directly; no invented anecdote. |
| Client voice / avoid-list (no politics, no AI-slop) | PASS | Both platform reviews confirm voice match and zero AI-slop phrasing; no political content. |
| Platform-native structure (LinkedIn) | PASS | Per linkedin-review.md. |
| Platform-native structure (Instagram) | PASS | Per instagram-review.md, including 5-tag hashtag cap. |
| Hook strength and readability | PASS | Both hooks stand alone within their platform's truncation limit and are grounded in the actual research. |
| Image relevant, original, style-guide-consistent, correctly sized | **NEEDS HUMAN DECISION** | See below — no curated room mockup exists for this entry, and the image could not be downloaded/cropped in this sandbox. |
| Alt text accurate, matches final image/post | **NEEDS HUMAN DECISION** | Alt text is based on catalog description + metadata only, not a direct view of the photo — flagged as not visually verified in both alt-text files. |
| Tags/mentions appropriate, minimal, no unwanted third-party tagging | PASS | LinkedIn: zero tags (justified). Instagram: 5 tags at the cap, all relevant, no third-party tags. |
| Compliance constraints from client profile | PASS | No professional/medical/legal claims; no price quoted (price_note flagged it as currently "on sale," unconfirmed). |
| No secrets/API keys/private info in output | PASS | Checked all files in this topic folder — none present. |

## NEEDS HUMAN DECISION items (both apply to the image, same root cause)

1. **No `chosen_images` curated for "Where She Cried Flower Grew."** No
   human or Claude session has visually confirmed which of this
   listing's photos (if any) is a styled room mockup versus a flat
   product shot. This run used `primary_image_url` (a square, 780x780
   product photo per catalog metadata) for both platforms, per the
   routine's explicit fallback instruction, rather than guessing. Agata
   (or a future session with visual access) should view this listing's
   photos, pick a mockup index if one exists, and add `chosen_images` to
   the catalog entry for future use.
2. **Image was not downloaded or cropped to platform dimensions.** Egress
   to `images.squarespace-cdn.com` failed (CONNECT tunnel 403) on a
   single test; per run instructions this was not retried. The raw
   `primary_image_url` was passed directly to Buffer uncropped and
   un-letterboxed — Buffer's own servers will fetch it independently.
   This also means the Instagram image is not actually cropped to the
   platform's 1080x1350 ratio; it will post at whatever aspect ratio the
   source photo has (square-ish, 780x780 original, though Squarespace
   CDN URLs can often be requested at other sizes — not verified here).
   Alt text for both platforms is explicitly flagged as written from
   catalog metadata, not a direct view of the image.

## Status update

`status.json` set with linkedin and instagram at "review-ready," no
FAIL items. Package is ready to present and to stage as Buffer drafts
(Step 11) — both NEEDS HUMAN DECISION items above must be surfaced
prominently in the run summary and the Step 13 email, not buried.

## Addendum (post-Buffer-staging)

3. **Instagram channel shows `isDisconnected: true` in `list_channels`**,
   unresolved since at least post 036 — this is now at least the 12th
   consecutive run where this has been true. The Instagram draft itself
   still came back clean on `get_post` (status draft, nothing
   scheduled), consistent with every prior run, so this did not block
   staging — but a disconnection flag sitting unresolved for this long
   warrants a human checking Buffer's Instagram connection directly,
   since an actual disconnection would eventually block real publishing
   even though drafting still works.
