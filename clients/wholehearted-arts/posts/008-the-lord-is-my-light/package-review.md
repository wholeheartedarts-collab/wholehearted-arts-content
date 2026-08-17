# Content package review — "The Lord is My Light" (008)

Covers all three platform variants (LinkedIn, Instagram, Facebook)
together, per CLAUDE.md's Step 10.

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal clear and match brief | PASS | Painting = "The Lord is My Light" (Studio Collection); audience = art collectors; takeaway = Psalm 27:1's trust-amid-fear, not fear's absence; tone matches brand-voice.md for all three platforms. |
| Every factual claim supported | PASS | Pulled from fact-check.md — no UNSUPPORTED items remain; two issues (a comparative size claim, an unhedged historical claim) were caught and fixed during platform review, documented in fact-check.md and linkedin-review.md. |
| Balanced treatment where topic has real risks/drawbacks | PASS (N/A-ish) | Devotional/art topic, not a claims-heavy topic like the AI-automation pillar — research.md's "Risks/limitations" section is about source-verification risk (price staleness, paraphrase-vs-verbatim, no-invented-backstory), and all three drafts respect those limits (no price/availability stated, paraphrase correctly framed, no invented Agata backstory beyond the one real catalog quote). |
| No fabricated facts, quotations, personal experiences, results | PASS | Confirmed via fact-check.md. The devotional/reflective framing ("I wanted this piece to hold...") is first-person interpretive voice consistent with prior approved posts (003-007), not a claimed fact or third-party result. |
| Client voice and avoid-list rules followed | PASS | No politics anywhere. No AI-slop phrasing flagged in any platform review. Voice matches brand-voice.md's warm/personal/first-person guidance for the art-collector register on all three platforms. |
| Platform-native structure and current requirements met | PASS | Pulled from linkedin-review.md, instagram-review.md, facebook-review.md — all three PASS with no open items. |
| Hook strength and readability | PASS | LinkedIn hook 200 chars (< 210 cutoff), Instagram hook 56 chars (< 125 cutoff), Facebook hook is a clear grounded opening line — all verified in their respective platform-review files. |
| Image relevant, original, consistent with style-guide.json, correctly sized | **NEEDS HUMAN DECISION** | This uses a real photo of Agata's own existing painting (not a Gemini-generated image), which is the correct path per image-generation's "real image" allowance and matches posts 002-007's pattern — so "original" and "relevant" are satisfied by definition (it's the actual artwork). However: local download/crop was **not possible this run** — wholeheartedarts.com, static1.squarespace.com (http and https), and images.squarespace-cdn.com were all tested live this run and confirmed blocked (see images/README-source-image.md). No platform-specific crop (LinkedIn 1200x627, Instagram 1080x1350 portrait, Facebook 1200x630) exists. The raw catalog image_url is used as a fallback — safe for the Buffer/Instagram push (Buffer's servers fetch it independently), but there is no locally-sized file for LinkedIn or Facebook manual posting. A human should either source/crop the image manually before manual-posting LinkedIn/Facebook, or confirm the uncropped source image is acceptable as-is. |
| Alt text accurate, matches final image and post | **NEEDS HUMAN DECISION** | All three alt-text files were written from the catalog's text description only, not from direct visual inspection of the image file (same blocked-CDN reason above), and are explicitly flagged as not visually verified in each alt-text file. A human should visually confirm the alt text against the actual image before or shortly after publishing. |
| Tags/mentions appropriate, minimal, not forced, no unwanted third-party tagging | PASS | LinkedIn: none (with rationale). Instagram: exactly 5, real mix. Facebook: 1 (brand tag only). No third parties tagged anywhere. |
| Compliance constraints from client profile respected | PASS | No professional/medical/legal claims present; nothing in profile.md's compliance section applies to a devotional art post. |
| No secrets, API keys, or private information anywhere in the output package | PASS | Confirmed — no environment variables, keys, or private data written into any file in this topic folder. |
| Price/availability accuracy (topic-specific addition, given catalog staleness) | **NEEDS HUMAN DECISION** | research.md flags the catalog's $80 price and availability as an unverified 2026-08-10 snapshot; live wholeheartedarts.com re-check failed again this run (EGRESS_BLOCKED). No draft states the price or availability, so this doesn't block the current text — but if Agata wants to add a price/link when posting manually, she should verify current price/availability herself first. |

## Summary

**No FAILs.** Three NEEDS HUMAN DECISION items, all stemming from the
same root cause (this sandbox's confirmed egress block to
wholeheartedarts.com and its image CDN, re-tested and re-confirmed this
run):

1. No locally cropped/sized image exists for any platform — raw catalog
   URL used as fallback (fine for Buffer/Instagram; a gap for manual
   LinkedIn/Facebook posting).
2. Alt text was written from the catalog's text description, not
   verified against the actual image file.
3. The $80 price/availability is an unverified 2026-08-10 snapshot,
   should be confirmed by Agata before ever being stated publicly (moot
   for this specific package since no draft currently states it).

All three platform drafts (LinkedIn, Instagram, Facebook) individually
PASS their platform-fit reviews, and the shared fact-check found no
unsupported claims. Package is **review-ready**, pending the three flagged
items above for Agata's awareness.
