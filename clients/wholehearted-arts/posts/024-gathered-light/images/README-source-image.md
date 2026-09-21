# Image source — 024 "Gathered Light"

No locally generated or cropped image files in this folder. Egress to
the Squarespace CDN (`images.squarespace-cdn.com`) is blocked in this
sandbox (confirmed this run: one Python `urllib` download attempt
returned `Tunnel connection failed: 403 Forbidden`; not retried, per
run instructions).

**Image used for all three platforms:** the catalog's verified room
mockup —

```
https://images.squarespace-cdn.com/content/v1/5b412dba5ffd201a3f9205e4/1778036673026-VNNJXF67LMJ0IWLR2I7I/DCB1AB99-DB71-4535-8641-F028BB96D9D1.png
```

This is `chosen_images.mockup_url` (index 1) from
`painting-catalog.json`'s "Gathered Light" entry — a human/Claude
verified-by-viewing living room mockup with the gold frame reading
clearly. `chosen_images.avoid_indexes: [0]` (a bad two-room composite
crop) was respected; index 0 was not used anywhere.

The raw, uncropped URL was passed straight through to Buffer for all
three platform items (Buffer's own servers fetch the image
independently of this sandbox, per run instructions). No local
cropping to LinkedIn 1200x627 / Instagram 1080x1350 / Facebook
1200x630 was possible this run — flagged as a NEEDS HUMAN DECISION
item in `package-review.md` and in the Step 13 email.
