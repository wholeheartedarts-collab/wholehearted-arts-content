# Content Package Review: "Together we go further" (LinkedIn + Instagram)

## NEEDS HUMAN DECISION items (read first)

1. **Atelier Collection selection is still blocked — 8th consecutive run
   falling back to Studio.** Atelier's only remaining catalog "unused"
   entry, "Let Our Light Continue to Shine," is an explicit prayer for
   peace in Israel and the Jewish people. Every run since post 039
   (039, 040, 041, 042, 043, 044, 045, and now 046) has judged this too
   politically/religiously sensitive for unattended selection and fallen
   back to Studio instead, even though the deterministic selection rule
   says both collections should be drawn from. This is now a recurring,
   unresolved condition, not a one-off judgment call — a human needs to
   either (a) make an explicit call on "Let Our Light Continue to Shine"
   (post it, exclude it permanently, or have Agata write it herself), or
   (b) add new Atelier pieces to the catalog, or the pipeline will keep
   defaulting to Studio indefinitely.
2. **No `chosen_images` mockup exists for "Together we go further."**
   `primary_image_url` (a flat/undifferentiated product photo per the
   catalog, filename suggests but does not confirm a styled room shot)
   was used for both platforms instead of a confirmed room mockup, per
   this run's documented fallback. A human should view the product's 5
   photos and set `chosen_images` for this entry so future posts (and a
   possible re-crop of this one) can use a confirmed mockup.
3. **Image could not be downloaded or cropped.** Sandbox egress to
   `images.squarespace-cdn.com` returned a 403 at the proxy (tested once,
   not retried, per run instructions). The raw external URL was passed
   directly to Buffer for both platforms instead of a cropped,
   platform-sized file. Alt text is written from catalog text/filename
   only and is explicitly flagged as not visually verified in both
   `alt-text/linkedin.md` and `alt-text/instagram.md`.
4. **Recurring Buffer Instagram channel disconnection (per prior posts'
   status.json history, posts 036-045) should be re-checked this run.**
   Carried forward as a known open item to verify fresh in Step 11 below,
   not re-asserted as still true without checking.

## Checklist

| Check | Verdict | Notes |
|---|---|---|
| Topic/audience/takeaway/tone/goal clear and match brief | PASS | Faith + friendship testimony, art-collector audience, matches research.md's chosen angle. |
| Every factual claim supported | PASS | Pulled from fact-check.md — no UNSUPPORTED claims. |
| Balanced treatment where topic has real risks/drawbacks | N/A | Reflective/testimony topic, not an argument with counterarguments (consistent with research.md's "no stats/risks applicable" note). |
| No fabricated facts, quotes, personal experiences, or results | PASS | Story stays within Agata's own catalog description; no invented friend, diagnosis, or scene. Scripture quoted and verified (fact-check.md). |
| Client voice and avoid-list rules followed | PASS | No politics; no AI-slop phrasing (linkedin-review.md, instagram-review.md both PASS on this). |
| Platform-native structure/format requirements met | PASS | Pulled from linkedin-review.md (PASS) and instagram-review.md (PASS). |
| Hook strength and readability | PASS | Both hooks grounded in the real story, distinct from each other, within each platform's character cutoff. |
| Image relevant, original, consistent with style-guide, correctly sized | NEEDS HUMAN DECISION | Relevant and original (Agata's real product photo, not AI-generated or a copied reference) — but not confirmed-mockup and not cropped to platform dimensions (see items 2-3 above). Not a FAIL: this is the documented, sanctioned fallback for blocked egress / missing curation, not an error in this run's process. |
| Alt text accurate and matches final image/post | PASS (with flag) | Alt text matches what's actually known about the image and plainly discloses it is not visually verified — accurate about its own limitation rather than overclaiming. |
| Tags/mentions appropriate, minimal, not forced, no unwanted third-party tagging | PASS | LinkedIn: none. Instagram: 5, relevant mix, no third parties tagged. |
| Compliance constraints from client profile respected | PASS | No professional/medical/legal claims made; "vision difficulty" left in Agata's own general language, not diagnosed. |
| No secrets/API keys/private information anywhere in package | PASS | Reviewed all files above; none present. |

## Verdict

**Review-ready.** No FAILs. Four NEEDS HUMAN DECISION items recorded
above — none blocks presenting the package, but all four should be
surfaced prominently to Agata (see Step 13 email) rather than buried.
