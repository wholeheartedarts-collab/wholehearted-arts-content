# Image source — 006-united-in-prayer

**No local image files in this folder this run.** Both image CDN hosts
were tested and are blocked in this sandbox (2026-08-12, same run as the
main-domain egress test):

- `static1.squarespace.com` (http) — `curl` returned HTTP 403.
- `static1.squarespace.com` (https) — `curl` CONNECT tunnel failed, 403.
- `images.squarespace-cdn.com` (https) — `curl` CONNECT tunnel failed, 403.

Local download/crop via Pillow (the pattern used in posts 003/004) was
not possible. Per the documented fallback, this post uses the **raw
public image URL directly** wherever an image is needed, rather than a
locally cropped/letterboxed file:

```
http://static1.squarespace.com/static/5b412dba5ffd201a3f9205e4/5f11d41be38d9c085e833c02/6402636328ae6f101f317a68/1719797355687/F6FD04DF-48F8-49BB-AC87-D622C3B7ABEC?format=1500w
```

(source: `painting-catalog.json`, "United in Prayer", Studio Collection —
original product photo, not this pipeline's own crop.)

## Per-platform implication

- **Instagram**: this raw URL is passed directly to Buffer's
  `create_post` as the image attachment — Buffer's own servers fetch it
  independently of this sandbox, so the CDN block here does not block
  Buffer's ability to attach it. Not cropped to Instagram's 1080x1350
  portrait spec this run — it's the original product photo (24"x18"
  painting per catalog, so the source photo is likely landscape-ish, not
  pre-cropped to Instagram's portrait ratio).
- **LinkedIn / Facebook**: not pushed to Buffer this run regardless (see
  publishing-handoff limitation). When Agata handles these manually, hand
  her this same raw URL (or ask her to save the original product photo
  from her own site) rather than a pipeline-cropped file — no
  locally-generated crop exists to hand off.

## Flag for a future run

If egress to the CDN host(s) is ever unblocked, this topic's images
should be regenerated properly (downloaded, cropped/letterboxed per
platform dimensions with a background color sampled from the source
photo, per the style guide) rather than left as raw-URL-only.
