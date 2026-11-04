# Content Package Review — 048 "The Spiral of Time" (LinkedIn + Instagram)

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal clear and match brief | PASS | Art-collector audience, faith/trust-in-God's-timing takeaway, reflective tone consistent across both platforms. |
| Every factual claim supported | PASS | Pulled from `fact-check.md` — no UNSUPPORTED claims; one claim tightened during drafting to stay in subjective-voice territory. |
| Balanced treatment of risks/limitations | N/A | Not a topic with real drawbacks/counterarguments (art/faith reflection, not the AI-automation pillar) — research.md's limitations section covers interpretive risk (over-reading an abstract piece), which was respected by keeping the copy close to the catalog's own language. |
| No fabricated facts, quotes, personal experiences, or results | PASS | No invented backstory, no third-party reaction claimed, no invented statistic. See fact-check.md. |
| Client voice / avoid-list (no politics, no AI-slop) | PASS | No political content. No generic hype phrasing. Emoji removed from the Instagram draft to match brand-voice.md's "minimal emoji, none required" default. |
| Platform-native structure / LinkedIn format | PASS | See linkedin-review.md — full PASS on first draft. |
| Instagram platform fit (hook length, hashtag cap, link handling) | PASS | See instagram-review.md — full PASS on first draft; exactly 5 hashtags, no raw links. |
| Hook strength and readability | PASS | Distinct hooks per platform (not reused), both grounded in the painting's own description. |
| Image relevant, original, on-style, correctly sized | **NEEDS HUMAN DECISION** | See "Image note" below — no `chosen_images` exists for this painting, and the image could not be downloaded/cropped in this sandbox. |
| Alt text accurate and matches final image/post | **NEEDS HUMAN DECISION** | Alt text (alt-text/linkedin.md, alt-text/instagram.md) is built from catalog text + image metadata, not direct visual inspection — flagged as not visually verified. |
| Tags/mentions appropriate, minimal, no unwanted third-party tagging | PASS | LinkedIn: no tags (none needed). Instagram: 5 relevant tags, no third parties tagged. |
| Compliance constraints from client profile | PASS | None specified beyond no-politics/no-fabrication, both respected. |
| No secrets/API keys/private info in output | PASS | Confirmed — no keys, no internal data beyond what's in the public catalog. |

## Image note (NEEDS HUMAN DECISION)

- This painting ("The Spiral of Time") has **no `chosen_images` field**
  in painting-catalog.json — no human or prior Claude session has
  reviewed its 5 product photos to identify a styled room mockup.
  Per the run's instructions, a mockup was **not guessed**; the entry's
  `primary_image_url` (a flat/square product photo, ~2461x2500, per
  catalog metadata) is used for **both** LinkedIn and Instagram instead.
  This is the same situation as post 047.
- This sandbox's egress to `images.squarespace-cdn.com` failed (CONNECT
  tunnel 403), tested once and not retried per the run's instructions.
  The image was **not downloaded or cropped** to either platform's
  target dimensions (LinkedIn 1200x627/1200x1200; Instagram 1080x1350).
  The raw `primary_image_url` was passed directly to Buffer for both
  platforms — Buffer's own servers fetch images independently of this
  sandbox, so this is expected to still resolve correctly in the draft
  (to be confirmed via `get_post` in Step 11).
- Alt text for both platforms is based on the catalog's written
  description and image metadata (shape, color palette as described),
  not on direct visual inspection, and says so explicitly.
- **Ask for Agata:** (1) pick a mockup index for "The Spiral of Time" (or
  confirm the flat product shot is fine for this piece), and (2) if
  convenient, re-check both Buffer drafts' image rendering once posted,
  since the native ~2461x2500 crop wasn't reshaped to either platform's
  ideal aspect ratio.

## Process note (NEEDS HUMAN DECISION — escalating)

- Collection-selection rule: catalog's raw used-counts are tied/stale,
  so the rule reconciles against actual post history. Atelier Collection
  has had **zero genuinely free, non-flagged candidates for 10
  consecutive runs now** (posts 039–048) — its only unused entry, "Let
  Our Light Continue to Shine," is an explicit prayer for peace in Israel
  and the Jewish people and has been treated as NEEDS HUMAN DECISION
  since post 039 rather than auto-selected.
- This run selected from Studio Collection again (painting: "The Spiral
  of Time," reconciled against all 47 existing post folders to confirm
  it was genuinely unused, in stock, visible on the live site, and
  carried no caution flag).
- **This has now run 10 times in a row without Agata's input on the
  underlying question.** Recommend she either (a) explicitly clear "Let
  Our Light Continue to Shine" for automated use, (b) direct a human to
  write that piece herself, or (c) add more Atelier paintings to the
  catalog — otherwise every future run will keep defaulting to Studio,
  which is itself a quiet policy decision that deserves her sign-off
  rather than remaining implicit.

## Status set by this review

`linkedin`: review-ready. `instagram`: review-ready. `facebook`:
not-needed (Instagram cross-posts to the Facebook Page). See
`status.json`.
