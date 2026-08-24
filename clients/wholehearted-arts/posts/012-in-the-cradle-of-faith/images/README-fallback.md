# Image fallback note — topic 012 "In the Cradle of Faith"

The sandbox egress proxy blocked `images.squarespace-cdn.com` this run
(`curl` returned `CONNECT tunnel failed, response 403`), consistent with
the known block on this domain. Per run instructions, this is not treated
as a run failure.

**Fallback used:** the catalog's public `image_url` is passed directly
wherever an image URL is needed (Buffer specifically, since Buffer's own
servers fetch the image independently of this sandbox):

```
https://images.squarespace-cdn.com/content/v1/5b412dba5ffd201a3f9205e4/1716644040722-6LQ04SLIW9HKCZ1YXTR1/08C1B477-350A-4E6B-9818-C751A1647CF0.jpeg
```
(verbatim from `painting-catalog.json`, re-confirmed via grep before use in Buffer to avoid transcription error.)

**Consequences of this fallback:**
- No local per-platform crops were produced (no `linkedin-v1.png`,
  `instagram-v1.png`, `facebook-v1.png` in this folder) — unlike posts
  003/004, which had live image access.
- The same uncropped source image (at its native aspect ratio) will be
  used across all three platforms via Buffer, rather than a LinkedIn
  1200x627 crop, an Instagram 1080x1350 portrait crop, and a Facebook
  1200x630 crop.
- Alt text (see `../alt-text/`) is written from the catalog's textual
  description only and is explicitly flagged as not visually verified —
  Agata should confirm/correct it against the real painting.

This is recorded here, in `package-review.md`, `status.json`, the final
run summary, and the Step 13 email, per run instructions.
