# Image fallback note — 014 "Cleansing Waters - Divided by Grace"

The image CDN (images.squarespace-cdn.com) is blocked by the sandbox
egress proxy — confirmed this run via a single `curl` attempt (`CONNECT
tunnel failed, response 403`), consistent with the known block documented
in prior runs (e.g. posts 012, 013). Not retried, per run instructions.

No local download or Pillow crop was possible this run. Per the run
instructions, the fallback is to pass the raw public image URL directly
wherever an image URL is needed:

https://images.squarespace-cdn.com/content/v1/5b412dba5ffd201a3f9205e4/1765165151889-4H5ZLUXN1E0J0JGVY73S/940528D1-CB8A-4B8A-98EE-1AD6243EF48C.jpeg

This is safe for Buffer specifically, since Buffer's own servers fetch the
image independently of this sandbox. No platform-sized crops (LinkedIn
1200x627 / Instagram 1080x1350 / Facebook 1200x630) exist for this topic —
all three platforms will use the same raw source image via its public URL.

**NEEDS HUMAN DECISION:** Agata should review the actual image against
each platform's crop before publishing, since none of the platform-
specific crops/letterboxing described in CLAUDE.md's workflow could be
produced this run.
