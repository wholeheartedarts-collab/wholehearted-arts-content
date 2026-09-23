# Content package review — "Carrying Burden, Seeking Light"

Covers all three platform variants (LinkedIn, Instagram, Facebook)
produced for this topic together.

| Check | Verdict | Notes |
|---|---|---|
| Topic, audience, takeaway, tone, goal clear and match brief | PASS | Art-collector audience, faith/emotion/healing pillar, consistent across all three drafts. No AI-automation content mixed in. |
| Every factual claim supported | PASS | Pulled from fact-check.md — no UNSUPPORTED claims across any draft. |
| Balanced treatment of real risks/drawbacks | N/A | Not applicable — single-artwork piece, not a claims-heavy topic (research.md's "Risks/limitations" section covers fabrication risk, which was respected, not a pro/con topic). |
| No fabricated facts, quotations, personal experiences, results | PASS | Confirmed in fact-check.md; scripture pairing explicitly framed as editorial, not Agata's stated inspiration; no invented studio anecdote or specific relationship claim. |
| Client voice and avoid-list rules followed (no politics, no AI-slop) | PASS | All three platform reviews passed this individually; no political content anywhere. |
| Platform-native structure per platform review | PASS | linkedin-review.md, instagram-review.md, facebook-review.md all PASS with no open items. |
| Hook strength and readability | PASS | Confirmed per-platform in each review file. |
| Image relevant, original, consistent with style-guide.json, correctly sized | **NEEDS HUMAN DECISION** | Image is a real, non-AI-generated photo of Agata's own painting (appropriate — this is her own product photography, not a copied third-party reference). However: (1) this catalog entry has no `chosen_images` block, so the flat/primary product photo is used rather than a room mockup — no mockup exists to select; (2) egress to the image CDN was blocked, so the raw uncropped source (2500x2500) was **not** cropped to platform dimensions (LinkedIn 1200x627, Instagram 1080x1350, Facebook 1200x630) or checked against style-guide.json's placeholder guidance. See `images/README-source-image.md`. |
| Alt text accurate, matches final image and post | **NEEDS HUMAN DECISION** | Alt text (alt-text/linkedin.md, instagram.md, facebook.md — identical, same image on all 3 platforms) was written from the catalog's product description and image metadata, not from direct visual inspection, since the image could not be downloaded/viewed this run. A human should visually confirm it matches once viewed. |
| Tags/mentions appropriate, minimal, no unwanted third-party tagging | PASS | LinkedIn 2 tags, Instagram 5 tags (at cap, real mix), Facebook 1 tag — all with stated rationale, no third parties tagged. |
| Compliance constraints from client profile respected | PASS | No professional/medical/legal claims; no compliance constraints apply to this art-pillar topic. |
| No secrets, API keys, or private information in the output package | PASS | Reviewed all files this run — none present. |

## Summary

**Two NEEDS HUMAN DECISION items, both about the image** (same root
cause as posts 023 and 024 — sandboxed egress to
`images.squarespace-cdn.com` is blocked):

1. No `chosen_images` mockup exists for this painting, and the raw
   image could not be downloaded/cropped to per-platform dimensions
   this run — the uncropped source URL was passed through to Buffer as
   a fallback (Buffer fetches independently of this sandbox).
2. Alt text was written from the product description and metadata, not
   from direct visual inspection of the image, and should be confirmed
   by a human once they can see it.

No FAIL items. All text content (research, three platform drafts, fact
-check) passes cleanly.
