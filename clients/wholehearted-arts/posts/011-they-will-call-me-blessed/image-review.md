# Image sourcing — 011-they-will-call-me-blessed

## Source

Real product photo of the painting "They Will Call Me Blessed" (Atelier
Collection) — not an AI-generated image, per the established pattern for
this pipeline (real photos of Agata's own paintings, same as posts
002-010).

**Image URL (from `painting-catalog.json`):**
`http://static1.squarespace.com/static/5b412dba5ffd201a3f9205e4/69da327c2622e42cafbe8437/647eb639b790816d9cc2ecb5/1686025789576/07D63B10-71D2-4C19-8514-70EBBF2138C8?format=1500w`

## Download attempt — FAILED (egress blocked)

```
curl -sS -o /dev/null -w "%{http_code}" "http://static1.squarespace.com/...?format=1500w"
```

Result: HTTP 403 over plain HTTP; a follow-up HTTPS attempt failed at the
CONNECT tunnel stage (also 403). Confirms `static1.squarespace.com` is
still blocked this run, consistent with every run since 2026-08-19.
`www.wholeheartedarts.com` was also tested this run (one WebFetch) and
returned `EGRESS_BLOCKED`.

## Fallback used

Per CLAUDE.md's Step 7-9 fallback instructions: no local per-platform
image files were produced (no `linkedin-v1`, `instagram-v1`, or
`facebook-v1` file in `images/`). The raw `image_url` above is passed
directly wherever a public image URL is needed — this is fine for Buffer
specifically, since Buffer's own servers fetch the image independently of
this sandbox (confirmed working in posts 005-010's `get_post` responses).

## Consequence for platform-specific sizing

No platform-specific crop/letterbox was applied (LinkedIn 1200x627,
Instagram 1080x1350 portrait, Facebook 1200x630, per
`visual-style/style-guide.json`). The same single raw source image is
used everywhere this run. This painting's real dimensions are 12" x 36"
— a narrow, panoramic vertical format, more extreme than most prior
pieces in this catalog — so the uncropped source image may read
particularly poorly on a 1:1 or landscape platform crop. A human should
apply a proper per-platform crop before final publish, and pay particular
attention to this piece's unusual aspect ratio when doing so.

## No caution flags on this catalog entry

"They Will Call Me Blessed" carries no `availability_note` or
`price_note` in the catalog — no additional flag needed beyond the
general catalog-staleness caveat already noted in research.md (price
$1,500, not independently reverified this run).

## Update after Buffer's Instagram draft was created

Buffer's own servers successfully fetched the source image (see Step 11)
and reported its actual dimensions: **1500 x 1501px — essentially
square**, not the extremely panoramic 12"x36" ratio the painting's own
physical dimensions would suggest. This likely means the product photo
is a straight-on square crop/thumbnail of the piece rather than a
full-frame photo matching its real proportions (common for e-commerce
listing photos). This softens (but does not remove) the aspect-ratio
concern raised below — a human should still visually confirm the photo
shows the whole piece before treating it as final for any platform.

## Visual verification

**Not visually verified this run.** The catalog's text description for
this specific entry is thinner than several other catalog pieces — it
names the scripture inspiration and construction materials but does not
describe visible colors, imagery, or composition. Alt text (see
`../alt-text/`) is written honestly from only what the catalog actually
states (medium, format, construction) rather than inventing visual
details (color palette, imagery, composition) that aren't in the source
text. A human should replace the alt text with a real visual description
once the actual photo can be viewed.
