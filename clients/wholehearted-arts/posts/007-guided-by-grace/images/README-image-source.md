# Image source note — "Guided by Grace"

**No local image file was produced this run.**

Attempted, in order:
1. Live fetch of the painting's product page on wholeheartedarts.com —
   blocked (EGRESS_BLOCKED, confirmed again 2026-08-14).
2. Direct download of the source photo from the Squarespace image CDN
   (`static1.squarespace.com`), via both `curl` (http and https) and
   WebFetch — also blocked: "Host not in allowlist: static1.squarespace.com."
   This confirms the 2026-08-10 catalog's open question ("untested as of
   2026-08-10") — the CDN is blocked the same as the main domain, at
   least from this sandbox.

**Fallback used (per run instructions):** the raw catalog `image_url` is
passed directly wherever a public image URL is needed, rather than a
locally cropped/letterboxed file:

```
http://static1.squarespace.com/static/5b412dba5ffd201a3f9205e4/69da327c2622e42cafbe8437/68c7345a1e42e41876a02285/1757885540239/828A1C89-CEF6-45EB-9226-DDE4BA0B78A0.jpeg?format=1500w
```

This is workable for the **Instagram Buffer draft** specifically, since
Buffer's own servers fetch the image independently of this sandbox's
egress restrictions. It is **not** a platform-correct crop for any
platform (no LinkedIn 1200x627, Instagram 1080x1350 portrait, or Facebook
1200x630 version was produced) — this is a real limitation of this run,
not a stylistic choice. A human (or a future run with working egress)
should still produce proper per-platform crops before final publish,
especially for LinkedIn and Facebook where no automated image handoff is
happening this run anyway.

Alt text (see `../alt-text/`) is written from the catalog's text
description only, and is explicitly flagged as not visually verified
this run, consistent with this same limitation.
