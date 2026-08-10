# Image source — 005-time-of-singing-has-come

**No local image files in this folder this run.** Both the image CDN
hosts were tested and are blocked in this sandbox
(2026-08-10, same run as the main-domain egress test):

- `static1.squarespace.com` — `curl` returned 403 /
  "Host not in allowlist" (agent-proxy egress block message).
- `images.squarespace-cdn.com` — `curl` returned 403 (CONNECT tunnel
  failed).

This matches the anticipated fallback in this run's task instructions:
local download/crop via Pillow (the pattern used in posts 003/004) was
not possible. Per the documented fallback, this post uses the **raw
public image URL directly** wherever an image is needed, rather than a
locally cropped/letterboxed file:

```
http://static1.squarespace.com/static/5b412dba5ffd201a3f9205e4/5f11d41be38d9c085e833c02/6a49be4966ff5c078a0e7603/1783217741454/103D0247-AFD0-4445-90F2-8F212102A64D.jpeg?format=1500w
```

(source: `painting-catalog.json`, "The Time of Singing Has Come",
Studio Collection — original product photo, not this pipeline's own
crop.)

## Per-platform implication

- **Instagram**: this raw URL is passed directly to Buffer's
  `create_post` as the image attachment — Buffer's own servers fetch it
  independently of this sandbox, so the CDN block here does not block
  Buffer's ability to attach it. Not cropped to Instagram's 1080x1350
  portrait spec this run — it's the original square (per catalog,
  painting is 20"x20", likely close to square already) product photo.
- **LinkedIn / Facebook**: not pushed to Buffer this run regardless (see
  publishing-handoff limitation). When Agata handles these manually,
  hand her this same raw URL (or ask her to save the original product
  photo from her own site) rather than a pipeline-cropped file — no
  locally-generated crop exists to hand off.

## Flag for a future run

If egress to the CDN host(s) is ever unblocked, this topic's images
should be regenerated properly (downloaded, cropped/letterboxed per
platform dimensions with a background color sampled from the source
photo, per the style guide) rather than left as raw-URL-only.
