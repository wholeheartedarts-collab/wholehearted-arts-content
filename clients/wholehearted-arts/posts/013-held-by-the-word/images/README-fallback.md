# Image fallback note — 013 "Held by the Word"

The image CDN (images.squarespace-cdn.com) is blocked by the sandbox egress
proxy — confirmed this run via `curl` (`CONNECT tunnel failed, response
403`), consistent with the known block documented in prior runs (e.g. post
012).

No local download or Pillow crop was possible this run. Per the run
instructions, the fallback is to pass the raw public image URL directly
wherever an image URL is needed:

https://images.squarespace-cdn.com/content/v1/5b412dba5ffd201a3f9205e4/1677101676936-FJ01UXROA3KDNY5GD27E/C9D6166C-1ECE-4FB1-B128-B24DF5581722

This is safe for Buffer specifically, since Buffer's own servers fetch the
image independently of this sandbox. No platform-sized crops (LinkedIn
1200x627 / Instagram 1080x1350 / Facebook 1200x630) exist for this topic —
all three platforms will use the same raw source image via its public URL.

**NEEDS HUMAN DECISION:** Agata should review the actual image against each
platform's crop before publishing, since none of the platform-specific
crops/letterboxing described in CLAUDE.md's workflow could be produced this
run.
