# Content package review: "Unexpected Happiness" (LinkedIn + Instagram)

Platforms covered: **LinkedIn, Instagram.** Facebook is intentionally not
produced — Agata's Instagram cross-posts automatically to her Facebook
Page (CLAUDE.md scope note, confirmed again by this run's instructions).

## NEEDS HUMAN DECISION — read first

1. **19 consecutive automated runs (posts 039-056) have now fallen back
   to the Studio Collection** because Atelier's only unused, non-flagged
   entry is "Let Our Light Continue to Shine" (an explicit prayer for
   peace in Israel/the Jewish people), independently judged
   politically-adjacent each time under the no-politics avoid-list. This
   run reconciled the catalog's stale `unused` list directly against post
   folders and confirmed every other nominal Atelier "unused" title
   already has a post. **This is a standing decision for Agata, not
   something another automated run should keep silently re-deciding.**
   She needs to choose one of: (a) explicitly approve using "Let Our
   Light Continue to Shine" despite the political-adjacency judgment, (b)
   confirm Atelier should be treated as exhausted until she adds new
   paintings to it, or (c) add new Atelier paintings to the catalog.
2. **No `chosen_images` set for "Unexpected Happiness."** Per the run's
   instructions, `primary_image_url` was used for both platforms instead
   of a human-verified room mockup. It is not confirmed whether this
   image shows the artwork alone or in a styled scene — a human should
   view the listing's photos and set `chosen_images` for this entry (and
   decide whether to regenerate the posts' images once a mockup is
   identified).
3. **Image could not be downloaded/cropped in this sandbox** —
   `images.squarespace-cdn.com` is blocked by the sandbox's egress proxy
   (tested once, not retried per instructions). The raw image URL was
   passed directly to Buffer for both platforms; neither image was
   cropped to the style-guide's platform dimensions (LinkedIn 1200x627,
   Instagram 1080x1350).

## Checklist

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal clear and matches brief | PASS | Art-collector/faith audience; "unexpected joy after a hard season" takeaway; matches research.md angle #1. |
| Every factual claim supported | PASS | See fact-check.md — all claims SOURCED, no UNSUPPORTED items. One hashtag medium error caught and fixed during review (see below). |
| Balanced treatment of real risks/drawbacks | PASS (N/A) | Not a topic with a "both sides" tradeoff (art/faith reflection, not a product or automation claim) — research.md's limitations section covers stock status and image-verification, both carried into this review rather than hidden. |
| No fabricated facts/quotes/personal experiences | PASS | Confirmed no invented personal anecdote; both drafts paraphrase only the catalog's own description and a verified scripture quote. |
| Client voice and avoid-list rules followed | PASS | No politics; no AI-slop phrasing; voice checked against brand-voice.md in both platform reviews. |
| Platform-native structure/format met | PASS | See linkedin-review.md and instagram-review.md, both PASS. |
| Hook strength and readability | PASS | Both hooks stand alone within platform character limits (verified in platform reviews). |
| Image relevant, original, on-style, correctly sized | **NEEDS HUMAN DECISION** | Relevant and original (real product photo, not a copied reference) — but not confirmed against style-guide.json's composition/mood guidance by direct view, no chosen_images mockup, and not cropped to platform dimensions due to egress failure. See items 2-3 above. |
| Alt text accurate, matches final image and post | **NEEDS HUMAN DECISION** | Alt text is based on the catalog's text description only, not direct visual inspection — flagged in both alt-text files. Should be re-verified once a human can view the actual image. |
| Tags/mentions appropriate, minimal, no unwanted third-party tagging | PASS | LinkedIn: none (correct, no discoverability gain). Instagram: exactly 5, relevant, no third parties tagged. |
| Compliance constraints respected | PASS | No professional/medical/legal claims made; no sale/availability claim given SOLD OUT status. |
| No secrets/API keys/private info in output | PASS | Checked all files in this topic folder — none present. |

## Overall verdict

**PASS, with 3 NEEDS HUMAN DECISION items** (the Atelier-exhaustion
pattern, the missing chosen_images, and the un-cropped/unverified image).
No FAILs. Package is ready to stage as Buffer drafts — not to be approved,
scheduled, or published by this run.
