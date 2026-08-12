# Content Package Review — 006-united-in-prayer

Covers LinkedIn, Instagram, and Facebook variants together.

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal clear | PASS | Prayer-over-house-and-family reading of Psalm 127:1, tied to Agata's Studio piece "United in Prayer"; art-collectors pillar; consistent tone across all three platform drafts. |
| Every factual claim supported | PASS | See fact-check.md — no UNSUPPORTED claims across all 3 drafts. |
| Balanced treatment of risks/limitations | PASS (n/a for tone, but see notes) | Not a data/persuasion topic, so no "drawbacks" to balance. The real limitation (thin narrative beyond Agata's one quoted sentence) was respected: no invented backstory (which family, what event) was added anywhere. |
| No fabricated facts/quotes/personal experiences | PASS | No invented anecdote or specific personal story; the "my prayer for all families" line is quoted directly from the catalog's record of Agata's own words, not expanded upon. |
| Client voice / avoid-list (no politics, no AI-slop) | PASS | All 3 platform reviews passed this individually; no politics anywhere. |
| Platform-native structure per platform | PASS | Confirmed via linkedin-review.md, instagram-review.md, facebook-review.md (all PASS). |
| Hook strength/readability | PASS | Each platform has its own appropriately-sized hook (LinkedIn ~210 char budget, Instagram ~116 char, Facebook clear opening line). |
| Image relevant, original, style-guide-consistent, correctly sized | **NEEDS HUMAN DECISION** | Image CDN egress was blocked this run (tested live: static1.squarespace.com http/https and images.squarespace-cdn.com https all returned 403 — see images/README-source-image.md). No local download, no crop/letterboxing was performed for any platform. The **raw original product photo URL** is used as-is for all platforms instead of a pipeline-generated/cropped image. It is relevant (it's the actual painting) but not resized/letterboxed per platform's dimensions spec in style-guide.json, and not visually inspected by this pipeline. Agata should confirm the raw photo looks right pushed as-is (particularly for Instagram, since it's about to go to Buffer as a real draft) before approving. |
| Alt text accurate, matches final image/post | **NEEDS HUMAN DECISION** | Written from the catalog's text description only, not from direct visual inspection, per alt-text/*.md's explicit flag. Should be visually confirmed/corrected by a human (or a future run with working image egress) before publish. |
| Tags/mentions appropriate, minimal, no unwanted third-party tagging | PASS | LinkedIn: none. Instagram: 5 relevant tags, at the cap. Facebook: 1 brand tag. No third-party tags anywhere. |
| Compliance constraints from profile respected | PASS | No professional/medical/legal claims; no politics; no fabricated results. |
| No secrets/API keys/private info in output | PASS | No keys or private info anywhere in the package. |
| Price/availability accuracy | **NEEDS HUMAN DECISION** | Painting price ($500) and product-page link come from the 2026-08-10 catalog snapshot, not a live fetch (wholeheartedarts.com and its image CDN are both still blocked in this sandbox, confirmed live this run). No price is stated in any of the three posts, but the LinkedIn and Facebook posts reference dimensions/signature details from the catalog and Facebook links directly to the product page — Agata should confirm the piece is still listed/available and the link still resolves before this goes out. |

## Summary

**No FAIL items.** Three **NEEDS HUMAN DECISION** items, all stemming
from this sandbox's continued blocked egress to wholeheartedarts.com and
its image CDN (confirmed blocked again this run, 2026-08-12):

1. Images are unresized raw-URL fallbacks, not pipeline-cropped/
   letterboxed per platform — visually confirm before approving,
   especially for the Instagram Buffer draft.
2. Alt text was written from text description only, not visual
   inspection — confirm/correct against the real image.
3. Price/availability of the painting (from a point-in-time catalog
   snapshot) and the dimensions/signature detail were not re-verified
   live — confirm before this goes out.

Package is otherwise ready for human review at `review-ready` status.
