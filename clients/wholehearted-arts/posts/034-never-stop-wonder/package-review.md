# Content Package Review: "034 — Never Stop Wonder" (LinkedIn + Instagram)

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal match brief | PASS | Art-collector/faith pillar, personal reflection on wonder as a spiritual discipline, consistent across both platform drafts. |
| Factual claims supported (from fact-check.md) | PASS | All claims SOURCED per `fact-check.md`; no UNSUPPORTED items. |
| Balanced treatment of risks/drawbacks | PASS (N/A) | Not a topic with real drawbacks/counterarguments to balance (art/faith reflection, not a claims-heavy topic) — research.md correctly notes this. |
| No fabricated facts/quotes/experiences | PASS | Scripture quotes verified via WebSearch against multiple independent citations; painting description drawn verbatim from the catalog listing; scripture-to-painting link explicitly framed as the writer's own reflection, not an Agata quote. |
| Voice/avoid-list (no politics, no AI-slop) | PASS | First-person, warm, concrete; no politics; no hype phrasing — confirmed in linkedin-review.md and instagram-review.md. |
| Platform-native structure (LinkedIn) | PASS | Per linkedin-review.md — hook 183 chars, short paragraphs, soft CTA, no forced hashtags. |
| Platform-native structure (Instagram) | PASS | Per instagram-review.md — hook 99 chars, caption fits the mockup image, exactly 5 hashtags, no clickable-link expectation. |
| Hook strength/readability (both) | PASS | Both hooks stand alone, grounded in research, not clickbait. |
| Image relevant/original/on-style/correctly sized | **NEEDS HUMAN DECISION** | This topic uses a **sourced real photo** (Agata's own existing room-mockup product photo for "Never Stop Wonder," `chosen_images.mockup_url`, index 0), per CLAUDE.md step 8's "source, if the human wants a real photo instead" and this run's explicit instruction to prefer the mockup. It is Agata's own copyrighted photo, not a copied third-party image, and not AI-generated — style-guide.json (placeholder) doesn't strictly apply to a sourced photo. **Could not crop to platform dimensions** (LinkedIn 1200x627, Instagram 1080x1350) — egress to `images.squarespace-cdn.com` was blocked in this sandbox (confirmed with one test attempt, not retried per instructions). The same uncropped source image is passed directly to Buffer by URL for both platforms; Buffer's own servers will fetch it independently. A human should confirm the uncropped image displays acceptably on both platforms, or crop it manually before publishing. |
| Alt text accurate, matches final image/post | **NEEDS HUMAN DECISION** | Alt text (linkedin.md, instagram.md) is based on the catalog's own listing description plus a *prior* human/Claude verification note for this exact mockup index ("idx 0 is airy mint-green with a rattan chair," verified 2026-09-01) — not a fresh visual check by this session, since image content could not be viewed in this sandbox. Alt text is almost certainly accurate (it rests on a real prior human-involved verification of this specific image), but a human should do a quick visual confirmation before/at publish time. |
| Tags/mentions appropriate, no unwanted third-party tagging | PASS | LinkedIn: none used (correct call). Instagram: exactly 5, relevant mix, no third-party tags. |
| Compliance constraints from profile respected | PASS | No professional/medical/legal claims; no fabricated CTAs beyond approved soft-CTA default. |
| No secrets/API keys/private info in output | PASS | Checked all files in this topic folder — no keys, tokens, or private info present. |

## Summary verdict

**Overall: PASS, with two NEEDS HUMAN DECISION items** (both about the image: uncropped due to blocked egress, and alt text not freshly visually verified this session). Neither is a FAIL — both are judgment calls flagged for Agata, consistent with the egress-fallback handling this routine explicitly anticipates. No other check failed. Package is **review-ready** for both platforms.
