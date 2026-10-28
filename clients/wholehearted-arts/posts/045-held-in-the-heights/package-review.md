# Content Package Review — 045 Held in the Hights (LinkedIn + Instagram)

## NEEDS HUMAN DECISION items (read first)

1. **Atelier Collection has been effectively unavailable for 8 runs
   straight (posts 038-045).** The catalog's own `unused` list for
   Atelier is stale: 10 of its 11 listed "unused" entries already match
   existing post folders, leaving only "Let Our Light Continue to
   Shine" — a Hanukkah/Israel-peace-prayer piece (sold out, on-sale-at-
   snapshot) that every run since post 039 has judged too close to the
   client's no-politics avoid-list to use without explicit sign-off, even
   though the catalog itself carries no `caution_note` flag on it. The
   practical effect is the opposite of Agata's explicit instruction
   ("Atelier must never be the silent default") — Studio has become the
   silent default for over two weeks of runs. Two fixes, either is a
   human call: (a) regenerate `painting-catalog.json` from the live
   Squarespace data so Atelier's unused list reflects reality, or (b)
   explicitly decide whether "Let Our Light Continue to Shine" is
   publishable content and update its `caution_note` accordingly either
   way. This routine is not resolving it unilaterally again.
2. **No `chosen_images` mockup exists for "Held in the Hights."** Per
   this run's instructions, Agata wants a room mockup used wherever one
   exists; none has been curated for this painting. `primary_image_url`
   (flat product photo, portrait orientation) was used for both
   platforms instead. Flagging for future `chosen_images` curation.
3. **Image not downloaded or cropped to platform dimensions.** Egress to
   `images.squarespace-cdn.com` failed (CONNECT tunnel 403), tested once,
   not retried per run instructions. The uncropped source URL was passed
   directly to Buffer for both platforms (Buffer fetches server-side,
   independent of this sandbox).
4. **Alt text not visually verified.** This sandbox cannot view image
   content; alt text for both platforms was written from the catalog's
   own title/description only. A human should confirm it against the
   actual photo.
5. **Minor: product title typo.** Agata's own site lists the title as
   "Held in the Hights" (missing "e"); both posts acknowledge this
   transparently in-copy rather than silently "fixing" her product title
   without her sign-off.

## Checklist

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/tone/goal clear and match brief | PASS | Art-collectors/faith pillar, matches research.md. |
| Every factual claim supported | PASS | See fact-check.md — all SOURCED, none UNSUPPORTED. |
| Balanced treatment of real risks/limitations | N/A | Reflective devotional art topic — no drawbacks requiring balance (research.md's "Risks" section covers production/process caveats only, already respected). |
| No fabricated facts/quotes/experiences | PASS | Confirmed in fact-check.md. |
| Client voice and avoid-list rules followed | PASS | See linkedin-review.md, instagram-review.md — no politics, no AI-slop. |
| Platform-native structure (LinkedIn) | PASS | linkedin-review.md — PASS on all items. |
| Platform-native structure (Instagram) | PASS | instagram-review.md — PASS on all items, hashtags capped at 5. |
| Hook strength and readability | PASS | Both hooks measured under their platform limits (LinkedIn 158/210, Instagram 95/125). |
| Image relevant, original, consistent with style guide, correctly sized | NEEDS HUMAN DECISION | Relevant and original (real product photo of the actual painting), but NOT cropped to style-guide.json's per-platform dimensions due to egress failure (item 3 above), and no mockup curated (item 2 above). |
| Alt text accurate, matches final image and post | NEEDS HUMAN DECISION | Written from description only, not visually verified (item 4 above). |
| Tags/mentions appropriate, minimal, no unwanted third-party tagging | PASS | LinkedIn: none used. Instagram: 5 relevant tags, no third parties tagged. |
| Compliance constraints respected | PASS | No professional/medical/legal claims; no politics. |
| No secrets/API keys/private info in output | PASS | Confirmed — no keys or private data in any file. |

**Overall: no FAIL items.** Five NEEDS HUMAN DECISION items recorded above and carried into status.json and the Step 13 email. Package is review-ready for both platforms.
