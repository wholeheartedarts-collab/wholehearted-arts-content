# Content Package Review — 049 "The Center Holds" (LinkedIn + Instagram)

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal clear and matches brief | PASS | Art-collector/faith pillar, single clear takeaway (rootedness under pressure), tone matches brand-voice.md. |
| Every factual claim supported | PASS | See fact-check.md — no UNSUPPORTED claims in either draft. |
| Balanced treatment of real risks/drawbacks | N/A | Not a risk/drawback-bearing topic (art/faith reflection, not the AI-automation pillar where balance is required). |
| No fabricated facts, quotes, personal experiences, results | PASS | Caught and corrected one drafting risk (LinkedIn draft originally implied Agata had Psalm 1:3 "in mind while painting" — not sourced; rewritten to present-moment reflective language before this review). |
| Client voice and avoid-list rules followed | PASS | No politics in either draft. Voice matches brand-voice.md (first person, concrete/sensory, no AI-slop phrasing). |
| Platform-native structure (LinkedIn) | PASS | See linkedin-review.md — full PASS. |
| Platform-native structure (Instagram) | PASS | See instagram-review.md — full PASS, hashtags at cap of 5. |
| Hook strength and readability | PASS | Both hooks are concrete, grounded in the real painting description, within each platform's standalone-truncation limit. |
| Image: relevant, original, consistent with style-guide, correctly sized | **NEEDS HUMAN DECISION** | This is a real product photo (not AI-generated, so style-guide.json doesn't directly apply), which is correct per the run's "use the real mockup/photo" instruction. BUT: this painting has no `chosen_images` entry in the catalog, so no human has confirmed whether any of its photos is a styled room mockup — `primary_image_url` (flat product shot) was used by default rather than guessed. Separately, egress to the image CDN is blocked in this sandbox, so no local crop was made for either platform; the same URL was passed straight to Buffer, uncropped, for both platforms. |
| Alt text accurate, matches final image and post | **NEEDS HUMAN DECISION** | Alt text (alt-text/linkedin.md, alt-text/instagram.md) is based on the catalog's written description only, since the image was never downloaded/viewed in this session — flagged in both files as not visually verified. Should be re-confirmed by a human (or a future run that can view the photo) once the image displays normally in Buffer. |
| Tags/mentions appropriate, minimal, no unwanted third-party tagging | PASS | LinkedIn: no tags (explained). Instagram: 5 relevant tags, no third parties tagged. |
| Compliance constraints from client profile respected | PASS | No professional/medical/legal claims made. |
| No secrets/API keys/private info in the output package | PASS | Checked — none present. |

## Additional NEEDS HUMAN DECISION item — painting/collection selection

This run's own reconciliation of `painting-catalog.json` against actual
post history found the catalog's used/unused tracking to be **very
stale** (nearly every entry on both collections' "unused" lists already
has a published post). Two items specifically need Agata's attention,
beyond this topic's own content:

1. **"Let Our Light Continue to Shine" (Atelier)** — the only
   genuinely-unused Atelier entry this run found, but its own catalog
   description is an explicit "prayer for peace in #Israel" with
   Hanukkah/Hebrew liturgical content. This run treated that as a
   politics-adjacent risk under the client's "no politics, even
   tangentially" rule and set it aside, even though the catalog's own
   `caution_note` on this entry is `None`. **Needs Agata's call**: either
   she's comfortable with this piece being used (in which case the
   catalog should be updated to say so explicitly), or she'd rather it
   stay excluded from the unattended pipeline permanently.
2. **Catalog data-quality gap**: at least three other entries carry
   real political content with no `caution_note` flag at all —
   "President Trump Portrait – customized!", "I Am Still Standing"
   (its own description: "Mixed Media of President Trump Likenesses"),
   and "Disassembled Grace" (explicit critique of "contemporary
   feminism"). This run excluded all three on its own judgment, but
   recommends the catalog be regenerated/corrected so future runs don't
   have to re-derive this by reading full entries one at a time.

Neither item blocks this topic's package — they're flagged for Agata's
decision and for catalog hygiene, not FAILs on "The Center Holds" itself.

## Result

**PASS, with 2 NEEDS HUMAN DECISION items** (image mockup selection /
alt-text visual verification) **plus 2 cross-cutting catalog items**
noted above for Agata's attention. No FAILs. Package is ready to present
at `review-ready` for both LinkedIn and Instagram.
