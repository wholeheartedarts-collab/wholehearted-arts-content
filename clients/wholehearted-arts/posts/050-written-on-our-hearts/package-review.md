# Content Package Review — Topic 050 "Prayerful Rose or Jeremiah"

Covers both platform variants (LinkedIn + Instagram). No Facebook
variant produced (Instagram cross-posts to the Facebook Page per
CLAUDE.md's current scope).

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal clear and match brief | PASS | Art-collector/faith pillar; takeaway is the stone-vs-heart contrast + forgiveness line; tone matches brand-voice.md. |
| Every factual claim supported | PASS | See fact-check.md — one misattributed detail (frame description) was caught and corrected during fact-check before this review; no UNSUPPORTED claims remain. |
| Balanced treatment of risks/limitations | PASS (N/A-leaning) | This is a devotional art piece, not a topic with real counterarguments to weigh (no "limitations" to balance, unlike the AI-automation pillar) — research.md states this explicitly rather than manufacturing a false balance. |
| No fabricated facts/quotes/personal experience | PASS | No invented backstory; scripture quoted/paraphrased accurately; no personal anecdote attributed to Agata. |
| Client voice and avoid-list rules followed | PASS | No politics; no AI-slop phrasing; checked against brand-voice.md. |
| Platform-native structure (LinkedIn) | PASS | See linkedin-review.md — full PASS. |
| Platform-native structure (Instagram) | PASS | See instagram-review.md — full PASS, hashtags at the 5-tag cap. |
| Hook strength and readability | PASS | Both hooks verified under their platform's character cutoff (LinkedIn 218 total/148 standalone-first-sentence; Instagram 60). |
| Image relevant, original, on-style, correctly sized | **NEEDS HUMAN DECISION** | No `chosen_images` exists for this catalog entry, so the flat product photo (`primary_image_url`) is used for both platforms rather than a room mockup — Agata has said she prefers mockups where one exists. A human should review this listing's other product photos and add a `chosen_images` entry (mockup_url / flat_url / avoid_indexes / note) to the catalog for future runs. Additionally, image download failed in this sandbox (egress to the Squarespace CDN blocked, tested once, not retried per run instructions) — the image was **not cropped to platform dimensions** (LinkedIn 1200x627 / Instagram 1080x1350) and was **not visually verified**; the raw CDN URL is passed straight to Buffer, whose own servers will fetch it independently. |
| Alt text accurate and matches final image/post | **NEEDS HUMAN DECISION** | Alt text (alt-text/linkedin.md, alt-text/instagram.md) is written from the catalog's text description only, since the image could not be viewed in this sandbox — flagged in both files as not visually verified. A human who can see the actual photo should confirm or correct the alt text once reviewed. |
| Tags/mentions appropriate, minimal, no unwanted third-party tagging | PASS | LinkedIn: none used (stated rationale). Instagram: 5 tags, all topic-relevant, no third parties tagged. |
| Compliance constraints respected | PASS | No price quoted (sale_price/price_note flagged, correctly avoided); no professional/medical/legal claim present. |
| No secrets/API keys/private info in output | PASS | Checked all files in this topic folder — none present. |

## Collection-selection decision carried forward — NEEDS HUMAN DECISION

Flagging again, as in posts 039 through 049: the Atelier Collection's
deterministic tiebreak selection has now pointed to Atelier for the
**12th consecutive run**, and its only non-duplicate unused entry
("Let Our Light Continue to Shine") remains a prayer for peace in
Israel/the Jewish people — treated as political-adjacent and excluded
each time rather than silently defaulting to Studio again. This is no
longer a one-off judgment call; it needs Agata's explicit decision:
either (a) confirm this piece should stay permanently excluded and have
the catalog's selection pool updated to drop it from consideration, or
(b) direct that it's acceptable to use with a specific, reviewed
framing, or (c) regenerate the catalog from the live Squarespace data to
add fresh Atelier inventory. See research.md's selection-reasoning
section for full detail.

## Summary

**Two open NEEDS HUMAN DECISION items** (image sourcing/mockup +
image not visually verified; the Atelier-exhaustion pattern, now 12
runs running). No FAIL items. Both platform drafts are otherwise ready
for Agata's review as Buffer drafts.
