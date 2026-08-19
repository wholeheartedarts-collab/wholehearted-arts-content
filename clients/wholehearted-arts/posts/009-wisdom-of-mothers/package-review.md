# Content package review — 009-wisdom-of-mothers

Full package gate covering LinkedIn, Instagram, and Facebook variants,
run 2026-08-19 (automated scheduled pipeline run).

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal clear and matches brief | PASS | Painting "Wisdom of Mothers" (Atelier Collection), Proverbs 31 generational-legacy angle, art-collector/faith pillar audience — consistent across all three drafts. |
| Every factual claim supported | PASS | Pulled from fact-check.md — no UNSUPPORTED or NEEDS SOFTENING items across any of the three platforms. |
| Balanced treatment of real risks/drawbacks | PASS | research.md's limitations section (Proverbs 31 sometimes misread as a rigid checklist) was deliberately woven into all three drafts rather than presenting an uncomplicated "ideal woman" framing — keeps the post encouraging rather than prescriptive. |
| No fabricated facts, quotations, personal experiences, or results | PASS | No specific personal anecdote about Agata's own family is claimed anywhere; all reflection stays general ("the women who did that for me," "mothers, grandmothers, and women of faith who shaped us"). |
| Client voice and avoid-list rules followed | PASS | Matches brand-voice.md across all three (first person, warm, sensory, no AI-slop). No politics anywhere. |
| Platform-native structure per platform review | PASS | linkedin-review.md, instagram-review.md, facebook-review.md all PASS — hook length, formatting, hashtag counts (LinkedIn: none needed; Instagram: exactly 5; Facebook: 0) all within this run's rules. |
| Hook strength and readability | PASS | Each platform opens with the same scriptural anchor (Proverbs 31:28) adapted natively per platform's truncation point and tone. |
| Image relevant, original, consistent with style-guide.json, correctly sized | **NEEDS HUMAN DECISION** | Image could not be downloaded this run — the CDN host (`static1.squarespace.com`) is blocked by sandbox egress, confirmed via a failed curl attempt (403, "Host not in allowlist") documented in image-review.md. No local files were produced, and **no platform-specific crops exist** (LinkedIn 1200x627, Instagram 1080x1350 portrait, Facebook 1200x630 per style-guide.json) — the same single raw source URL will be used everywhere. This is real and workable for the Instagram Buffer draft (Buffer fetches independently), but the image is not sized/cropped per style-guide.json for any platform, and its actual visual content has not been confirmed by this pipeline this run. **A human should view the real photo and confirm it's suitable before LinkedIn/Facebook are published, and ideally apply platform-specific crops.** |
| Alt text accurate and matches final image/post | **NEEDS HUMAN DECISION** | All three alt-text files are explicitly flagged as NOT visually verified this run — written from the catalog's text description only, since the image itself could not be downloaded. Content is plausible and matches the catalog's description closely, but **a human should confirm or correct the alt text against the actual photo before publishing**, per the flag already written into each alt-text file. |
| Tags/mentions appropriate, minimal, no unwanted third-party tagging | PASS | LinkedIn: none. Instagram: 5, all topic-relevant, no third parties tagged. Facebook: none. |
| Compliance constraints from client profile respected | PASS | No professional/medical/legal claims; no politics; price/availability not stated in any post copy (correctly sidesteps the unverified-this-run pricing question entirely). |
| No secrets, API keys, or private info in output package | PASS | Reviewed all files in the topic folder — no keys, tokens, or private information present. |

## Summary verdict

**No FAIL items.** Two **NEEDS HUMAN DECISION** items, both stemming
from the same root cause (image CDN egress blocked this run):

1. **Image not visually verified / not platform-cropped** — the real
   photo of "Wisdom of Mothers" could not be downloaded this run. The
   raw source URL is being used as-is (fine for the Instagram Buffer
   draft; Buffer fetches it independently), but it has not been cropped
   to LinkedIn/Instagram/Facebook dimensions, and this pipeline has not
   visually confirmed the image's actual content this run.
2. **Alt text not visually verified** — written from the catalog's text
   description only, for the same reason. Plausible but unconfirmed.

Neither blocks presenting this package for Agata's review, but both
should be resolved (or explicitly accepted) by a human before any of
these three posts is actually published — Agata should look at the real
product photo before LinkedIn/Facebook get sent out, since those are not
touched by this pipeline beyond `review-ready` status this run.
