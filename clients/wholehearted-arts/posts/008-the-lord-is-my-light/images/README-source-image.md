# Image source note — "The Lord is My Light"

This topic uses the artist's own real photo of the painting (per
CLAUDE.md's "use a real photo instead of a generated image when the
human/context calls for it" allowance, same pattern as posts 002-007),
not a Gemini-generated image — this is a real product photo of an
existing, already-created piece.

**Local download/crop was not possible this run.** Both
wholeheartedarts.com and its image CDN were tested live this run
(2026-08-17):

- `www.wholeheartedarts.com` — WebFetch, HTTP-level EGRESS_BLOCKED.
- `static1.squarespace.com` (http) — curl, HTTP 403.
- `static1.squarespace.com` (https) — curl, CONNECT tunnel failed / 403.
- `images.squarespace-cdn.com` (https) — curl, CONNECT tunnel failed / 403.

All four blocked. No local download, crop, or letterboxing (Pillow) was
possible this run — same outcome as posts 006 and 007.

**Fallback used:** the raw catalog `image_url` is passed directly
wherever a public image URL is needed. This is safe specifically for the
Buffer push (Instagram), since Buffer's own servers fetch the image
independently of this sandbox's egress restrictions — not the sandbox
downloading it.

Catalog image URL (Studio Collection, "The Lord is My Light"):
`http://static1.squarespace.com/static/5b412dba5ffd201a3f9205e4/5f11d41be38d9c085e833c02/6a46fc8a8d2fcd29fa1fd76b/1783037070284/5BBE35D7-8194-4AD0-8AD6-31A1DC384135.jpeg?format=1500w`

**Consequence:** no platform-specific crop/letterbox (LinkedIn 1200x627,
Instagram 1080x1350 portrait, Facebook 1200x630) exists for this topic.
The same raw square-ish source image would need to be used as-is for any
platform that requires a locally-hosted file — this affects LinkedIn and
Facebook manual posting more than Instagram (Buffer fetches the URL
directly for Instagram). Flagged as a NEEDS HUMAN DECISION item in
`package-review.md`.
