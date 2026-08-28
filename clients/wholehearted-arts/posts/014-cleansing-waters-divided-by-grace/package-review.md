# Content Package Review — 014 "Cleansing Waters - Divided by Grace"

Covers all three platform variants (LinkedIn, Instagram, Facebook)
produced for this topic together, per CLAUDE.md Step 10.

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal clear and matches brief | PASS | Art-collectors audience, faith/emotion/healing pillar, consistent across all three drafts (see each draft's "Angle used" section). |
| Every factual claim supported | PASS | Pulled directly from fact-check.md. One `UNSUPPORTED` claim (invented recency in the Facebook hook) was found and fixed before this review; no open UNSUPPORTED items remain. |
| Balanced treatment (risks/drawbacks) | N/A | Not a topic with real drawbacks/risks to balance for the reader (art/faith reflection piece, not a claims-heavy AI-automation topic). research.md's "Risks" section addresses a scripture-overclaiming pitfall for the writer, which was successfully avoided in all three drafts (verified in fact-check.md). |
| No fabricated facts/quotes/personal experiences | PASS | All scripture verified against multiple sources; the one invented detail (painting recency) was caught and removed. No other invented Agata anecdote — description content is the catalog's own text. |
| Client voice / avoid-list (no politics, no AI-slop) | PASS | Confirmed in each platform review. No political content; this painting and its description carry no political framing (unlike some other unused Atelier/Studio entries this run explicitly avoided selecting). |
| Platform-native structure per platform review | PASS | linkedin-review.md, instagram-review.md, facebook-review.md all PASS. |
| Hook strength and readability | PASS | Each hook grounded in the painting's own catalog description, correctly sized per platform (LinkedIn 147 chars, Instagram 101 chars, Facebook 126 chars — all measured and under their respective cutoffs). |
| Image relevant, original, style-guide consistent, correctly sized | **NEEDS HUMAN DECISION** | Image CDN (images.squarespace-cdn.com) blocked this run (confirmed via one untried-retry curl attempt, `CONNECT tunnel failed, response 403`). No download/crop was possible — all three platforms point to the same raw source image URL rather than platform-sized crops (LinkedIn 1200x627 / Instagram 1080x1350 / Facebook 1200x630). See `images/README-fallback.md`. style-guide.json is still a placeholder (no reference images yet), and this is a real product photo, not a generated one, so the style-guide dimension check doesn't fully apply either. |
| Alt text accurate and matches final image/post | **NEEDS HUMAN DECISION** | Alt text was written from the catalog's textual description only (`image_alt_from_site` is null for this entry) — not visually verified against the actual painting. Flagged in each `alt-text/[platform].md` file. |
| Tags/mentions appropriate, minimal, no unwanted third-party tags | PASS | LinkedIn 3, Instagram 5 (at cap), Facebook 1 — none tag third parties. |
| Compliance constraints respected | PASS | No professional/medical/legal claims. Facebook mentions price ($750) framed as "at last check," matching the catalog's current (non-sale, non-flagged) price — no stale-price risk on this entry, unlike post 013's. |
| No secrets/API keys/private info in output | PASS | Reviewed all files in this topic folder — no secrets present. |

## Summary of NEEDS HUMAN DECISION items (also going in the Step 13 email)

1. **Uncropped/unsized images.** All three platforms will use the same
   raw source image URL (not platform-sized crops) because the image CDN
   is blocked from this sandbox. Agata should review how it displays
   natively on each platform and consider swapping in a properly cropped
   version before or after publishing.
2. **Alt text not visually verified.** Written from the catalog's text
   description only. Agata should check it against the actual painting.

## Selection-rule note (not a content issue, but worth surfacing)

The painting catalog's own `used` counts are one to two posts stale (they
don't yet reflect posts 012 and 013, both Studio). This run manually
verified the real tally against posts 012/013's own files (not just the
catalog) before applying the tiebreaker, and confirmed Atelier was the
correct pick. Recommend Agata (or a future run) regenerate/update the
catalog's `used` lists so this reconciliation step isn't needed every run.

## Status

All three platform reviews and the fact-check PASS with no open FAILs.
The two NEEDS HUMAN DECISION items above are about image/alt-text
provenance, not content accuracy or brand-fit — the written content
itself is ready for human review. Nothing in this package is approved,
scheduled, or published by this run.
