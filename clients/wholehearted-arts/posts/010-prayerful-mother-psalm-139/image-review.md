# Image sourcing — 010-prayerful-mother-psalm-139

## Source

Real product photo of the painting "Prayerful Mother - Psalm 139"
(Studio Collection) — NOT an AI-generated image, per [[image-generation]]
skill's option to use a real photo of the client's own artwork instead
of generating one (same as posts 002 and 009).

**Image URL (from `painting-catalog.json`):**
`http://static1.squarespace.com/static/5b412dba5ffd201a3f9205e4/5f11d41be38d9c085e833c02/647f1c001d03d453653cef46/1686051846220/5C5032EA-EE8D-41EE-8C4D-3CB287B20172?format=1500w`

## Download attempt — FAILED (egress blocked)

```
curl -sS -o images/source-original.jpg "http://static1.squarespace.com/..."
```

Result: HTTP 403, response body: `Host not in allowlist:
static1.squarespace.com. Add this host to your network egress settings
to allow access.` Same block as confirmed in post 009 (2026-08-19) and
consistent with the wholeheartedarts.com block itself. This run
(2026-08-21) confirms the image CDN block persists.

## Fallback used

Per CLAUDE.md Step 7-9 fallback instructions: since local download and
Pillow-based cropping/letterboxing is not possible this run, no local
per-platform image files were produced (no `linkedin-v1`,
`instagram-v1`, or `facebook-v1` in `images/`). The raw `image_url`
above is passed directly wherever a public image URL is needed:

- **Buffer (Instagram draft):** the raw URL is attached directly to the
  `create_post` call — Buffer's own servers fetch the image
  independently of this sandbox's egress restrictions (confirmed working
  this way in post 009).
- **LinkedIn / Facebook:** not pushed to Buffer this run at all — left at
  `review-ready` for Agata to handle manually; she can pull the same
  photo directly from the live product page herself.

## Consequence for platform-specific sizing

No platform-specific crop/letterbox was applied (LinkedIn 1200x627,
Instagram 1080x1350 portrait, Facebook 1200x630, per
`visual-style/style-guide.json`). The same single raw source image is
used everywhere this run rather than three distinct optimized crops —
known deviation from the normal pipeline (posts 003/004), flagged here
and in the final run summary.
