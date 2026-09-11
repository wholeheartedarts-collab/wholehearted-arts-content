# Content Package Review — 020 The Strength of Three Strands

Covers all three platform variants (LinkedIn, Instagram, Facebook) for
this topic together.

| Check | Verdict | Notes |
|---|---|---|
| Topic, audience, takeaway, tone, goal clear and match brief | PASS | Art/faith pillar, marriage/covenant theme, art-collector audience, matches brief.md. |
| Every factual claim/statistic/example supported | PASS | Pulled directly from fact-check.md — no UNSUPPORTED items. |
| Balanced treatment where topic has real risks/drawbacks | PASS | research.md's limitations section (verse's original context vs. common marriage application) is respected — drafts frame the marriage reading as an interpretation/application, not the verse's sole original meaning. |
| No fabricated facts, quotations, personal experiences, results | PASS | All content traces to the artist's own catalog description or verified scripture/interpretation; no invented backstory. |
| Client voice and avoid-list rules followed | PASS | No politics; no AI-slop phrasing across all three drafts (confirmed in each platform review). |
| Platform-native structure per platform | PASS | linkedin-review.md, instagram-review.md, facebook-review.md all PASS with no open items. |
| Hook strength and readability | PASS | Each platform has its own tailored hook (not reused verbatim across platforms). |
| Image relevant, original, consistent with style-guide, correctly sized | **NEEDS HUMAN DECISION** | Image is the real product mockup photo (not Gemini-generated) per the run's explicit instruction to use `chosen_images.mockup_url` — this is a deliberate, human-directed real-photo path, not a shortcut (see [[image-generation]]'s "Using a real image instead" section). However, egress to images.squarespace-cdn.com was blocked, so the image could NOT be downloaded or cropped to each platform's dimensions (LinkedIn 1200x627 / Instagram 1080x1350 / Facebook 1200x630). The same raw, uncropped source URL is being passed to all three platforms. A human should re-crop/resize once local access to the image is available. |
| Alt text accurate, matches final image and post | **NEEDS HUMAN DECISION** | Alt text was written from the catalog's product description and the `chosen_images.note` field only — it was NOT visually verified against the actual image file, since the image could not be downloaded in this sandbox. A human should confirm the alt text matches the real photo before or shortly after publishing. |
| Tags/mentions appropriate, minimal, no unwanted third-party tagging | PASS | No third parties tagged or mentioned in any draft. |
| Compliance constraints from profile respected | PASS | No professional/medical/legal claims; no AI-automation claims (not applicable to this topic). |
| No secrets/API keys/private info anywhere in package | PASS | Confirmed — no keys or private data in any file. |

## Additional note carried from research

- The catalog's `availability_note` on this entry says it shows zero
  stock ("likely already sold"). No draft quotes a price or implies
  current availability — confirmed by re-reading all three final drafts.

## Overall verdict

**PASS, with two NEEDS HUMAN DECISION items** (both stem from the same
root cause: image CDN egress is blocked in this sandbox). No FAIL items.
Package is ready to present at `review-ready` per platform.
