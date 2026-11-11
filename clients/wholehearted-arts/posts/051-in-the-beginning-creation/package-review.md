# Content Package Review — "In the Beginning" (Creation Genesis 1:1-2)

Covers both platform variants (LinkedIn + Instagram) together.
Facebook: not produced (Instagram cross-posts to the Facebook Page as of
2026-09-30 — see CLAUDE.md / this run's scope override).

| Check | Verdict | Notes |
|---|---|---|
| Topic, audience, takeaway, tone, goal clear and match brief | PASS | Art/faith content pillar, art-collector audience, reflective "creation is ongoing" takeaway. Consistent across both platforms. |
| Every factual claim/statistic/example supported | PASS | See fact-check.md — no UNSUPPORTED claims. |
| Balanced treatment of real risks/drawbacks | N/A | Not a topic with risks/drawbacks to weigh (reflective art/scripture post, not an AI-automation claim). |
| No fabricated facts, quotations, personal experiences, results | PASS | No invented backstory; thin catalog description handled per skip_rules (shorter, image-led). |
| Client voice and avoid-list rules followed (no politics, no AI-slop) | PASS | See linkedin-review.md / instagram-review.md. |
| Platform-native structure / current format requirements met | PASS | Both platform reviews PASS on first draft. |
| Hook strength and readability | PASS | Confirmed in both platform reviews. |
| Image relevant, original, consistent with style-guide.json, correctly sized | **NEEDS HUMAN DECISION** | This catalog entry has **no `chosen_images` set** — no human/Claude has viewed its photos to pick a room-mockup vs. flat shot. Per this run's instructions, used `primary_image_url` (a flat product photo, 780x780) for both platforms rather than guessing which of the entry's 4 images (if any) is a styled mockup. Also: this sandbox's egress proxy blocks the Squarespace CDN (tested once per the run's egress note, not retried), so the image was **not downloaded, cropped, or letterboxed** to either platform's exact dimensions (LinkedIn 1200x627 / Instagram 1080x1350 per style-guide.json) — the raw source URL is being passed straight to Buffer, which fetches it independently. **Needs a human to: (1) confirm/select which of this entry's 4 photos should be used, and whether any is a mockup worth using instead of the flat shot, and (2) be aware the image in both Buffer drafts is uncropped.** |
| Alt text accurate, matches final image and post | **NEEDS HUMAN DECISION** | Alt text (alt-text/linkedin.md, alt-text/instagram.md) is written from the catalog's text description only, since the image could not be downloaded/viewed in this sandbox — explicitly flagged as NOT VISUALLY VERIFIED in both files. A human should check it against the actual photo in Buffer and correct if needed. |
| Tags/mentions appropriate, minimal, not forced, no unwanted third-party tagging | PASS | LinkedIn: none, with rationale. Instagram: 5 tags (at cap), relevant mix, no third-party tags. |
| Compliance constraints from client profile respected | PASS | No politics; no professional/medical/legal claims; no overstated sales language despite the piece showing sold out. |
| No secrets, API keys, or private information anywhere in the package | PASS | Confirmed — no credentials or private data in any file. |

## Additional NEEDS HUMAN DECISION item — recurring, escalated from post 050

**This is the 13th consecutive run (posts 039-051) selecting from the
Studio Collection because the Atelier Collection's catalog "unused" list,
once reconciled against actual post history, has been genuinely exhausted
of non-flagged candidates since post 044.** Its only remaining nominally
"unused" entry — "Let Our Light Continue to Shine" — is an explicit
prayer for peace in Israel and continues to be excluded as politically-
adjacent (client avoid-list).

Post 050 already raised this exact pattern as NEEDS HUMAN DECISION,
explicitly stating it "needs Agata's decision rather than another silent
Studio fallback." Nothing has changed since then (no catalog
regeneration, no new Atelier works added), so this run repeats the same
fallback — correctly, per the selection rule and the hard-stop rule
(which only triggers when **both** collections are exhausted, and Studio
is not) — but this is now flagged for the second time, more urgently,
because the pattern directly conflicts with Agata's repeated, explicit
instruction (2026-08-10, restated 2026-08-21) that she wants both
collections drawn from roughly evenly. **A human should either: (a) ask
Agata whether to regenerate/expand the Atelier catalog via her local
Squarespace MCP server, or (b) explicitly accept continued Studio-only
selection going forward and update the catalog's `_selection_rule`/
skip_rules accordingly so future runs stop re-flagging the same open
question.**

## Additional flag — sold out / zero stock

The selected painting shows **SOLD OUT / 0 in stock** at this catalog
snapshot ($180.00 list price, SKU SQ6536061). Neither draft implies it is
purchasable; no price or "shop now" language appears in either post. No
action required unless Agata wants this noted differently.

## Status

**Both platforms: review-ready.** No FAIL items — nothing here blocks
presenting the package, but the two NEEDS HUMAN DECISION items above
(image/mockup selection + the recurring Atelier-exhaustion flag) must be
surfaced prominently to Agata, not buried. Nothing in this package has
been approved, scheduled, or published.
