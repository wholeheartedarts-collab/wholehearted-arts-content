# Content Package Review — 005-time-of-singing-has-come

Covers LinkedIn, Instagram, and Facebook variants together.

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal clear | PASS | Season-change/renewal reading of Song of Solomon 2:12, tied to Agata's Studio piece; art-collectors pillar; consistent tone across all three platform drafts. |
| Every factual claim supported | PASS | See fact-check.md — no UNSUPPORTED claims across all 3 drafts. |
| Balanced treatment of risks/limitations | PASS (n/a for tone, but see notes) | This topic has no "drawbacks" in the research-limitations sense (not a data/persuasion topic) — the real limitation (thin narrative beyond one catalog paragraph) was respected: no invented backstory was added anywhere. |
| No fabricated facts/quotes/personal experiences | PASS | No invented anecdote, quote, or specific personal story; Polish-heritage line stays at the catalog's single-sentence level. |
| Client voice / avoid-list (no politics, no AI-slop) | PASS | All 3 platform reviews passed this individually; no politics anywhere. |
| Platform-native structure per platform | PASS | Confirmed via linkedin-review.md, instagram-review.md, facebook-review.md (all PASS). |
| Hook strength/readability | PASS | Each platform has its own appropriately-sized hook (LinkedIn ~200 char, Instagram ~105 char, Facebook clear opening line). |
| Image relevant, original, style-guide-consistent, correctly sized | **NEEDS HUMAN DECISION** | Image CDN egress was blocked this run (see images/README-source-image.md) — no local download, no crop/letterboxing was performed for any platform. The **raw original product photo URL** is used as-is for all platforms instead of a pipeline-generated/cropped image. It is relevant (it's the actual painting) but not resized/letterboxed per platform's dimensions spec in style-guide.json, and not visually inspected by this pipeline. Agata should confirm the raw photo looks right pushed as-is (particularly for Instagram, since it's about to go to Buffer as a real draft) before approving. |
| Alt text accurate, matches final image/post | **NEEDS HUMAN DECISION** | Written from the catalog's text description only, not from direct visual inspection, per alt-text/*.md's explicit flag. Should be visually confirmed/corrected by a human (or a future run with working image egress) before publish. |
| Tags/mentions appropriate, minimal, no unwanted third-party tagging | PASS | LinkedIn: none. Instagram: 5 relevant tags, at the cap. Facebook: 1 brand tag. No third-party tags anywhere. |
| Compliance constraints from profile respected | PASS | No professional/medical/legal claims; no politics; no fabricated results. |
| No secrets/API keys/private info in output | PASS | No keys or private info anywhere in the package. |
| Price/availability accuracy | **NEEDS HUMAN DECISION** | Painting price ($475) and product-page link come from the 2026-08-10 catalog snapshot, not a live fetch (wholeheartedarts.com and its image CDN are both still blocked in this sandbox). No price is stated in any of the three posts, but the Facebook post links directly to the product page — Agata should confirm the piece is still listed/available and the link still resolves before this goes out, in case availability or the URL has changed since the snapshot. |

## Summary

**No FAIL items.** Three **NEEDS HUMAN DECISION** items, all stemming
from this sandbox's continued blocked egress to wholeheartedarts.com and
its image CDN (confirmed blocked again this run, 2026-08-10):

1. Images are unresized raw-URL fallbacks, not pipeline-cropped/
   letterboxed per platform — visually confirm before approving,
   especially for the Instagram Buffer draft.
2. Alt text was written from text description only, not visual
   inspection — confirm/correct against the real image.
3. Price/availability of the painting (from a point-in-time catalog
   snapshot) and the Facebook product-page link were not re-verified
   live — confirm before this goes out, especially before any sale
   context is implied.

Package is otherwise ready for human review at `review-ready` status.
