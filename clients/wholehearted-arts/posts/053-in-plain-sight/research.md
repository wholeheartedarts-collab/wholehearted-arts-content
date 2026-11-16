# Research Brief: "In Plain Sight" (Studio Collection)

**Run type:** Automated scheduled pipeline run, 2026-11-16 (topic 053).

## Painting selection & collection reasoning (for the record)

- Catalog's raw `used_count` field reads Atelier 7 / Studio 7 (tied), but
  that field is stale per `_selection_rule`'s own warning. Reconciling
  against all 52 existing post folders (collection named in each post's
  research.md/linkedin-post.md/instagram-post.md header) gives the real
  picture: **Atelier used 18 times, Studio used 34 times** (post 052 was
  Studio). Per `_selection_rule` ("pick from the collection with fewer
  entries in its used list"), the reconciled count points to **Atelier**.
- Reconciled Atelier's `unused` list (11 entries) against the actual post
  folders: 10 of the 11 are already used under different post numbers
  (stale catalog data — e.g. "Guardian of Innocence" is post 016,
  "Patience" is 018, "Whimsical Gdansk" is 032). The sole remaining
  entry, **"Let Our Light Continue to Shine,"** is an explicit prayer
  for peace in Israel/the Jewish people woven into Hanukkah blessings —
  flagged as politically-adjacent by prior runs since post 039 and
  reconfirmed unchanged this run (now **15 consecutive runs**, 039-053,
  where Atelier has had zero viable candidates). It is also SOLD OUT (0
  in stock). **NEEDS HUMAN DECISION — carried forward again, unchanged.**
  Atelier's entire 18-painting catalog has now been fully used or
  flagged; it cannot supply a candidate until Agata either clears this
  flagged piece for use or the catalog is regenerated with new Atelier
  inventory.
- Per established precedent (posts 050 and 052's research.md, which
  document the identical fallback), **fell back to Studio Collection**,
  reconciling its 69-entry `unused` list against all 52 existing posts.
  Excluded as already-used-under-another-post-number (stale catalog
  data): "A Field Full of Yes" (043), "Breaking the Chains" (042), "In
  the Blossom" (044), "Held in the Hights" (045), "Together we go
  further" (046), "The Spiral of Time" (048), "The Center Holds" (049),
  "Prayerful Rose or Jeremiah" (050), "Creation Genesis 1:1-2" (051),
  "After the Rain, the Windows Kept Glowing" (052), plus the full set
  already excluded in posts 048/050/052 (season/holiday pieces, etc.).
- Excluded from this run's real candidates, beyond the already-used
  titles above (re-confirmed, not re-litigated — same reasoning as
  prior runs):
  - **"I Am Still Standing"** — named US political figure's likeness.
    Political.
  - **"Disassembled Grace"** — explicit culture-war framing of
    "contemporary feminism." Political under a different name.
  - **"Where the Walls Remember"**, **"The Key Within"** — Holocaust/
    Auschwitz remembrance theming, catalog-flagged/adjacent.
  - **"The Color of Waiting," "Flower of Righteousness"** — Agata's own
    unconfirmed personal health/vision-narrative pieces.
  - **"Mother"** — too close a duplicate of post 010 ("Prayerful Mother
    — Psalm 139").
  - **"Sisters"** — Agata already posted about this piece organically.
  - **"Happy Hanukkah," "Christmas Cards," "President Trump Portrait"**
    — explicitly political or off-season/off-brand.
  - **"Roses Blooms - Tissue Box Holder," "International Shipping
    Deposit"** — not actual artworks.
  - **"Life," "Tell Me Your Story," "The Language Beneath the Noise"**
    — `is_visible: false` in the live storefront per the catalog's own
    field, not purchasable, excluded on that basis.
  - **"Eyes of Fear - War"** — catalog description explicitly depicts a
    mother and child "amidst a chaotic and violent backdrop," framed
    around war/conflict imagery. Not flagged by any `caution_note`, but
    war/conflict-zone visual framing reads as adjacent to real-world
    geopolitical conflict in a way that sits too close to the client's
    no-politics-even-tangentially rule for a routine run to decide
    alone. **New finding this run — flagging for a human to judge; not
    selected.**
  - **"All the Love We Need," "Deep Blue Love," "Floral Symphony,"
    "Heart Filled with Sunrise," "Inner Wisdom," "Moonlight Serenade,"
    "Peace is Her Power," "Quiet Abundance," "Quiet Company,"
    "Reckoning," "Snowy Bond," "Unexpected Happiness," "Village"** — all
    SOLD OUT (0 in stock) at catalog snapshot. Usable in principle (a
    sold piece can still be shown and discussed), but passed over in
    favor of an in-stock piece so the post can carry a real, current
    purchase path if a collector asks.
  - **"Gaslighted," "Modern Man #1," "Red," "Woman"** — in stock, no
    caution flags, but catalog description is just medium/size (no
    narrative, no series, no scripture) with no clearly on-brand faith/
    healing angle to anchor a non-thin post.
- **Selected: "In Plain Sight"** (Studio Collection, SKU SQ2632555). In
  stock (1), explicitly tagged in the catalog's own description as
  "Painting from the original series **Heart of Healing**" — a direct,
  confirmed match to the client's stated content pillar of faith,
  healing, and overcoming struggles while staying faithful to God. No
  `caution_note`. Clean of any political/personal-health-narrative/
  duplicate issue. Not previously used (confirmed: no post folder
  mentions "In Plain Sight" or "Heart of Healing").
  - **Flag for Step 13 email: `price_note`** — "ON SALE at time of
    snapshot — verify before quoting any price in a post." Catalog
    shows list price $600, sale price $300. **Do not quote either price
    in the post** without Agata confirming current pricing; the post
    below avoids stating a price for this reason.
  - **Flag for Step 13 email: no `chosen_images`.** This entry has no
    human-verified mockup selection. Per the routine's instructions,
    `primary_image_url` is used as a flat product photo, and neither
    the post nor the alt text asserts it is a room scene. A human should
    view the listing's 11 photos and set `chosen_images` for future
    runs.

## Executive summary

"In Plain Sight" is an unframed, 24"×24" acrylic-on-canvas piece from
Agata May'kowska's Studio Collection, explicitly identified in the
product catalog as part of her original "Heart of Healing" series. The
catalog listing itself carries no further narrative — no artist
statement, no scripture citation, no backstory — only the medium, size,
finish, and series name. That absence of a given story is itself the
honest starting point for this post: rather than inventing a personal
account of what the title or the "Heart of Healing" series means to
Agata, this topic uses the title and series name as the occasion to
reflect on a real, well-documented scriptural theme — that God sees and
tends to pain that often goes unaddressed even while it sits in plain
view — and invites Agata's own audience to bring their own meaning to
the piece rather than being told what it "is about."

## Key points

- The painting's catalog record is thin by design of the data available
  (not a flaw in this research): medium, size, finish, series name only.
  No claim should be made about what the painting visually depicts
  beyond what the catalog states, since no human or AI in this pipeline
  has viewed the actual image (see Step 7-9 note on `chosen_images`).
- "Heart of Healing" as a named series is a real, verifiable fact from
  the live catalog data (Squarespace Commerce API snapshot) — this is
  the one concrete, sourced anchor for the post's angle.
- The title "In Plain Sight" lends itself naturally to a theme already
  present in this client's confirmed content pillars (faith, healing,
  overcoming struggles while staying faithful to God): the idea that
  struggle is often visible to others — carried openly, "in plain
  sight" — while still going unacknowledged or untended, and that
  Scripture repeatedly describes God as near to exactly that kind of
  open, visible brokenness.
- Two scripture passages anchor this honestly and are verified below
  (Psalm 147:3, Psalm 34:18). Both are about God actively drawing near
  to and healing visible brokenness — a direct, non-strained fit for
  "In Plain Sight" / "Heart of Healing" without requiring any invented
  backstory.

## Notable statistics

None applicable — this is an art/faith reflection topic, not a
statistics-driven topic. No statistics are used or needed in the post.

## Specific examples

None invented. The only "example" referenced is the painting itself
(title, series, medium, size, price status), each fact pulled directly
from the live catalog snapshot and cited in `sources.md`. No personal
anecdote, customer story, or specific result is claimed anywhere in this
package, consistent with the no-fabrication rule since Agata has not
supplied a backstory for this piece.

## Risks, counterarguments, or limitations

- **Thin source material.** The catalog gives no artist statement for
  this specific piece. The post must stay honest about that by framing
  itself around the *series name and title* plus verified Scripture,
  not by inventing what Agata "meant" by the piece. This is the
  deliberate, image-led, shorter approach the catalog's own skip_rules
  call for with thin-narrative pieces.
- **Visual claims risk.** Because no one in this pipeline has viewed the
  actual image (see below), the post and alt text must not describe
  specific depicted content (colors, objects, composition) — only what
  the catalog text and metadata state.
- **Pricing risk.** The listing is mid-sale at snapshot time and the
  snapshot could be stale by the time this post goes out. The post
  avoids quoting a price; any price question from a commenter should be
  answered by Agata directly, not pre-empted here.
- **Stock risk.** Only 1 unit in stock. If the post drives a sale
  inquiry and the piece sells before Agata checks, that's a normal
  single-edition-art risk, not a research gap — flagged so Agata isn't
  surprised.

## Possible content angles

1. **"Seen, not just seen through"** — contrasting being looked at
   (visible, "in plain sight") with being truly seen and tended to;
   ties title + series name to Psalm 147:3 / Psalm 34:18. *(Selected —
   see linkedin-post.md / instagram-post.md.)*
2. A studio-practice angle about what "Heart of Healing" as a named
   series suggests about Agata's broader body of work — would require
   more information about the series than the catalog provides; not
   used this run to avoid speculation about a series the catalog
   doesn't otherwise describe.
3. A direct product/collector-CTA angle leading with price and
   availability — not used, since the price is mid-sale/unverified and
   stock is down to the last unit; leading with an unstable number is a
   worse choice than a reflection angle that still naturally invites
   collectors to ask.

## Source list

1. Psalm 147:3 (ESV) — "He heals the brokenhearted and binds up their
   wounds." Verified via WebSearch result text against ESV.org,
   BibleGateway, and BibleHub snippets (direct fetch to esv.org,
   biblegateway.com, biblehub.com all blocked by this sandbox's egress
   proxy — WebSearch snippet text used instead, per this run's
   instructions). Search confirms this exact wording is consistent
   across ESV 2016 and 2025 text editions.
2. Psalm 34:18 (ESV) — "The LORD is near to the brokenhearted and saves
   the crushed in spirit." Verified the same way — WebSearch snippet
   text confirms this wording from ESV.org and BibleGateway listings.
3. Catalog entry "In Plain Sight," Studio Collection, SKU SQ2632555 —
   `clients/wholehearted-arts/painting-catalog.json` (sourced from the
   live Squarespace Commerce API). Product URL:
   https://www.wholeheartedarts.com/studio-collection-agata-christian-art/p/p549qpmp98z9a5wawxe1dmzt4411oi
   (fetch blocked by sandbox egress — confirmed by one direct WebFetch
   test this run per instructions, not retried; all facts below are
   taken from the catalog JSON snapshot, which is itself sourced from
   the live API, not from this blocked fetch attempt).
   - Medium: Acrylic on canvas, coarse finish, unframed, 24"×24".
   - Series: "Heart of Healing" (original series name, as stated in the
     catalog listing text).
   - List price: $600 USD; sale price at snapshot: $300 USD
     (`price_note`: ON SALE at time of snapshot — verify before quoting
     any price).
   - Availability: 1 in stock at snapshot.
   - `caution_note`: none.

## Research notes

- Everything about the painting's meaning, backstory, or specific visual
  content beyond "medium/size/series/price/stock" is **not sourced** and
  is therefore deliberately absent from the post — this is the
  skip_rules' "keep it shorter and image-led rather than inventing
  backstory" instruction applied directly.
- The scripture connection is this researcher's own synthesis (pairing
  verified scripture with the painting's title/series), clearly labeled
  as such in the post rather than presented as if Agata stated it
  herself.
- The Atelier-collection exhaustion finding and the "Eyes of Fear - War"
  flag are carried into `package-review.md` and the Step 13 email as
  NEEDS HUMAN DECISION items, not resolved here.
