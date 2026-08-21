# Image source — "They Will Call Me Blessed"

**No local crop/letterbox was produced this run.** Both hosts were
re-tested live this run and confirmed blocked in this sandbox:

- `www.wholeheartedarts.com` — EGRESS_BLOCKED (WebFetch)
- `static1.squarespace.com` — HTTP 403 over both http and https (curl)

## Fallback used

The raw catalog image URL is passed directly wherever a public image URL
is needed (works for Buffer, since Buffer's own servers fetch the image
independently of this sandbox — confirmed working in posts 005-010's
`get_post` responses):

```
http://static1.squarespace.com/static/5b412dba5ffd201a3f9205e4/69da327c2622e42cafbe8437/647eb639b790816d9cc2ecb5/1686025789576/07D63B10-71D2-4C19-8514-70EBBF2138C8?format=1500w
```

No platform-specific crop (LinkedIn 1200x627, Instagram 1080x1350
portrait, Facebook 1200x630 letterbox) was produced. The same uncropped
source image is used for all three platforms. The painting's real
dimensions are 12" x 36" (a narrow vertical/panoramic format per the
catalog) — a human should confirm how the uncropped source image reads
on each platform's aspect ratio before publishing, since this format is
more extreme than most prior pieces in this catalog.

Alt text (see `../alt-text/`) was written from the catalog's text
description only, not from direct visual inspection — flagged as not
visually verified in each alt-text file.
