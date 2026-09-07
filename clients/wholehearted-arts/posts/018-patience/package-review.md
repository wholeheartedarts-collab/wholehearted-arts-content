# Content Package Review — 018 "Patience"

Covers all three platform variants (LinkedIn, Instagram, Facebook)
together.

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal clear, matches brief | PASS | Art-collector pillar, faith/patience theme, Psalm 27:14 anchor consistent across all three platform variants, each rewritten fresh for its platform. |
| Every factual claim supported (per fact-check.md) | PASS | fact-check.md: all claims SOURCED or confirmed-absent; no UNSUPPORTED items. |
| Balanced treatment of real risks/limitations | N/A | Not an applicable check for this topic (no product claims, no automation-results claims requiring counterbalance — research.md's "risks/limitations" section covers process-narrative and translation-variance cautions, both already respected: no invented backstory, direct quote used rather than paraphrase). |
| No fabricated facts/quotes/personal experiences | PASS | Confirmed in fact-check.md — no personal Agata story, timeline, or third-party reaction invented in any draft. |
| Client voice / avoid-list (no politics, no AI-slop) | PASS | All three platform reviews (linkedin-review.md, instagram-review.md, facebook-review.md) passed this individually; no political content anywhere. |
| Platform-native structure per platform review | PASS | linkedin-review.md, instagram-review.md, facebook-review.md all PASS with no open items. |
| Hook strength and readability | PASS | Each platform has its own hook grounded in the Psalm 27:14 research angle, not generic; verified per-platform review. |
| Image relevant, original, consistent with style-guide.json, correctly sized | **NEEDS HUMAN DECISION** | Correct image was identified (catalog `chosen_images.mockup_url`, index 4 — a human-verified room mockup, navy wall/blue velvet sofa, no seasonal or avoid-index issue). Relevant and consistent with style-guide.json (warm tones, single focal point). **However**: could not be downloaded or cropped to platform dimensions (LinkedIn 1200x627 / Instagram 1080x1350 / Facebook 1200x630) this run — egress to images.squarespace-cdn.com is blocked (confirmed via one failed request, not retried per run instructions). The raw, uncropped source image will be passed directly to Buffer for all three platforms. A human should review how the uncropped image actually displays on each platform and, if needed, crop/regenerate locally. |
| Alt text accurate, matches final image and post | **NEEDS HUMAN DECISION** | Alt text (alt-text/linkedin.md, instagram.md, facebook.md) was written from the catalog's textual description and the human-verified `chosen_images.note` ("idx 4 (navy wall, blue velvet sofa) makes the oranges sing," confirmed 2026-09-01), not from direct visual inspection of the image file — same egress block as above. Content is well-grounded (not guessed) but a human should visually confirm it against the actual image. |
| Tags/mentions appropriate, minimal, no unwanted third-party tagging | PASS | LinkedIn 3 tags, Instagram 5 tags (at cap), Facebook 1 tag — all relevant, no third-party mentions. |
| Compliance constraints from client profile respected | PASS | No professional/medical/legal claims; no politics; no fabricated AI-automation claims (topic doesn't touch that pillar). |
| No secrets/API keys/private info in output | PASS | Checked all package files — none present. |
| **Catalog data integrity** | **NEEDS HUMAN DECISION** | `painting-catalog.json` is stale: it still lists "Guardian of Innocence" (used in post 016) and "What Grace Grows" (used in post 017) under their collections' `unused` lists, so both collections' `used_count` are undercounted by 1. This run cross-checked actual post-folder history against the catalog to correct for it (both collections were really tied at 8 used each, not 7-7 as the file shows — the tiebreaker outcome was unaffected this run, but a future run could pick a title that's actually already been used if this isn't fixed). A human should regenerate the catalog from the live Squarespace MCP server, or manually move these two entries to `used`. |

## Summary

**3 NEEDS HUMAN DECISION items — none are FAILs, all are staged safely:**
1. Catalog file (`painting-catalog.json`) is stale by two entries (016, 017) — needs regeneration/manual fix before the next run to avoid a future duplicate pick.
2. Image could not be downloaded/cropped to platform dimensions — uncropped source URL will go to Buffer as-is.
3. Alt text was written from text sources only, not visually verified against the actual image file.

No FAIL items. All three platform drafts pass their individual platform
reviews and the shared fact-check. Package is **review-ready**.
