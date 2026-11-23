# Images: "Unexpected Happiness"

No image file is stored in this folder. Per the run's egress note, a
single download attempt against the chosen image URL failed
(`images.squarespace-cdn.com` CONNECT tunnel returned 403) and was not
retried, per instructions.

- **Image used for both LinkedIn and Instagram:** `primary_image_url`
  from the catalog entry (no `chosen_images` exists for this painting —
  see research.md and package-review.md for the NEEDS HUMAN DECISION
  flag).
- **URL:**
  https://images.squarespace-cdn.com/content/v1/5b412dba5ffd201a3f9205e4/1764900339012-2NQS0F46DO8AK2L7FOX3/FB7C9362-7F18-4E88-9511-A7D11C341C87.jpeg
- This exact URL was passed directly to Buffer's `create_post` calls as
  the image source for both platforms (Buffer's own servers fetch it
  independently of this sandbox). Neither platform's image was cropped
  to the style guide's per-platform dimensions (LinkedIn 1200x627,
  Instagram 1080x1350) — the uncropped original was used, as the run
  instructions direct when egress fails.
- No new version should overwrite this note — if a human later downloads
  and crops this image manually, save it as `linkedin-v1.png` /
  `instagram-v1.png` per the standard convention and update this README.
