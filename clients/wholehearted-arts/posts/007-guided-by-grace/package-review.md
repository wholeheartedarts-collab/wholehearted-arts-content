# Content Package Review — 007-guided-by-grace ("Guided by Grace")

Covers all three platform variants (LinkedIn, Instagram, Facebook)
together, per CLAUDE.md's package-review convention.

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal clear, matches brief | PASS | Painting "Guided by Grace" + Psalm 34, art-collectors pillar (faith/healing/overcoming struggles), consistent across all three drafts. |
| Every factual claim supported | PASS | See `fact-check.md` — one unsupported superlative found in the Instagram hook and fixed during factual-verification; everything else traces to sourced material. |
| Balanced treatment where topic has real risks/drawbacks | N/A | Not a risk/drawback-bearing topic (unlike the AI-automation pillar); no one-sidedness concern applies here. |
| No fabricated facts, quotations, personal experiences, results | PASS | No invented Agata backstory or quote; research.md explicitly notes none was available and none was added. |
| Client voice / avoid-list (no politics, no AI-slop) | PASS | Confirmed in each platform review; no political content anywhere. |
| Platform-native structure per platform | PASS | LinkedIn, Instagram, and Facebook reviews each returned PASS with no revisions needed (Instagram required one factual-verification fix, now applied). |
| Hook strength and readability | PASS | Each platform's hook is grounded in the sourced David/Psalm 34 background and platform-appropriate in length. |
| Image: relevant, original, consistent with style-guide, correctly sized | **NEEDS HUMAN DECISION** | No local image file could be produced this run — both wholeheartedarts.com and its Squarespace CDN (static1.squarespace.com) are blocked from this sandbox (confirmed live this run, not assumed). Per the run's explicit fallback instructions, the raw catalog `image_url` is used directly instead of a locally cropped/letterboxed file. This works for the Instagram Buffer draft (Buffer fetches server-side) but means **no platform-correct crop exists for LinkedIn (1200x627) or Facebook (1200x630)**, and the Instagram image is uncropped/unverified rather than a proper 1080x1350 portrait crop. See `images/README-image-source.md`. Agata should confirm the image looks right before any platform goes live, and ideally a future run with working egress (or a manual upload) should produce real per-platform crops. |
| Alt text accurate, matches final image and post | **NEEDS HUMAN DECISION** | Written from the catalog's text description only, since the image was never visually inspected this run (see above). Each `alt-text/[platform].md` file explicitly flags this. Agata should confirm the description against the real painting before publishing. |
| Tags/mentions appropriate, minimal, not forced | PASS | LinkedIn: none. Instagram: 5, capped correctly. Facebook: 1. No third-party tagging anywhere. |
| Compliance constraints from client profile respected | PASS | No professional/medical/legal claims; no specific CTAs pushed beyond profile's soft-CTA default. |
| No secrets/API keys/private info in output | PASS | Confirmed across all files. |
| Facebook CTA link verification | **NEEDS HUMAN DECISION** | The product link in `facebook-post.md` (to the piece's page on wholeheartedarts.com) is the real URL recorded in the 2026-08-10 catalog snapshot but could not be live-verified this run (same egress block). Agata should click-check it before this post goes live. |

## Overall verdict

**Ready for human review, with three NEEDS HUMAN DECISION items** (all
stemming from the same root cause — this sandbox's confirmed egress
block to wholeheartedarts.com and its image CDN, not a quality defect in
the writing or research). No FAIL items. All copy, research, and
fact-checking are complete and passed cleanly.

Nothing in this package has been scheduled or published. Per CLAUDE.md,
only Instagram is being pushed to Buffer as an unscheduled draft (see
`status.json` and the run summary) — LinkedIn and Facebook remain at
`review-ready` for Agata to handle manually.
