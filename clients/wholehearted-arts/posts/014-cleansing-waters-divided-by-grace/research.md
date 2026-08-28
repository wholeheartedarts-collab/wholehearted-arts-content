# Research Brief: "Cleansing Waters - Divided by Grace" (Atelier Collection)

**Run type:** Automated scheduled pipeline run, 2026-08-28.

**Selection rule applied:** Per `painting-catalog.json`'s `_selection_rule`,
pick from the collection with fewer entries in `used`; if tied, pick
whichever collection was NOT used for the most recent post number. The
catalog itself (regenerated 2026-08-21) shows Atelier=6 used, Studio=4
used — but two posts have run since that snapshot and aren't reflected in
the catalog's `used` lists: post 012 ("In the Cradle of Faith," Studio) and
post 013 ("Held by the Word," Studio). Accounting for both, the real tally
is **Atelier=6, Studio=6 — a tie.** The tiebreaker applies: the most recent
post (013) drew from Studio, so this run picks the collection **NOT** used
most recently — **Atelier**. Verified directly against posts 012 and 013's
own files, not just the catalog, since the catalog is known to lag real
picks by a run or two.

**Painting/product details source:** `clients/wholehearted-arts/painting-catalog.json`,
regenerated 2026-08-21 directly from the live Squarespace Commerce API.

**Egress note:** A single WebFetch to www.wholeheartedarts.com was tested
this run and returned `EGRESS_BLOCKED`. Per instructions, not retried — all
painting facts below come from the catalog (itself live API data, not a
stale scrape).

## Painting details (from catalog, atelier.unused)

- **Title:** Cleansing Waters - Divided by Grace
- **Collection:** Atelier Collection ("Christian Abstract Art")
- **Price:** $750.00 USD — no `price_note`, no `sale_price`. Not on sale
  at time of snapshot.
- **Availability:** 1 in stock — no `availability_note` concern.
- **Medium:** Mixed media, black frame available now; white frame
  availability noted as "after January 4th" in the raw description (dated
  detail from the source listing — not restated as a current fact in the
  post, since "after January 4th" is ambiguous which year and may already
  have passed).
- **Dimensions:** 18" x 24" (per catalog description).
- **Product URL:** https://www.wholeheartedarts.com/atelier-collection-christian-abstract-art/p/tma307uwsxa7e321b36tqgkvto1rk8
  (not verified live this run — egress blocked; taken from catalog).
- **Image URL:** https://images.squarespace-cdn.com/content/v1/5b412dba5ffd201a3f9205e4/1765165151889-4H5ZLUXN1E0J0JGVY73S/940528D1-CB8A-4B8A-98EE-1AD6243EF48C.jpeg
- **Catalog description (verbatim):** "This striking abstract painting is
  divided into two realms. Above, a crowd stained with red symbolizes the
  burdens of sin and emotional turmoil. Below, figures gathered around a
  well of living water are portrayed in white, radiating purity and
  renewal. The vibrant blues evoke hope, contrasting sharply with the
  heaviness above. 'Cleansing Waters' powerfully illustrates the journey
  from darkness to light, inviting reflection on redemption and
  transformation."
- **No `caution_note` on this entry.**

## Executive summary

The painting's own catalog description does the heavy lifting here: a
two-realm composition (a red-stained crowd above, figures in white gathered
around a "well of living water" below) that visually stages redemption —
moving from the weight of sin toward renewal. "Well of living water" is not
generic imagery; it echoes a specific, well-documented biblical image
(Jesus offering "living water" in John 4, and the related "wells of
salvation" language in Isaiah 12:3), verified below. This fits the client's
faith/emotion/healing content pillar directly: redemption and
transformation, without needing any invented backstory.

## Key points

- The composition is literally divided top-to-bottom: red/burden above,
  white/purity below, with the "well of living water" as the pivot point
  between them — this is Agata's own structural description, not this
  brief's interpretation.
- "Living water" as an image for spiritual renewal has a specific, famous
  biblical source: John 4:10-14, where Jesus tells the Samaritan woman at
  the well that "whoever drinks of the water that I will give him will
  never be thirsty again... will become in him a spring of water welling
  up to eternal life" (ESV).
- A second, shorter verse carries closely related "water/salvation"
  imagery: Isaiah 12:3 (ESV) — "With joy you will draw water from the
  wells of salvation."
- Both verses are about water as a metaphor for what only God provides —
  which lines up with the painting's own "burdens of sin" → "purity and
  renewal" arc, without requiring the post to claim the painting is a
  literal illustration of either specific passage (the catalog description
  doesn't cite a verse number, so the post should treat the scripture as
  resonant context, not as a caption for what's literally painted).

## Notable statistics

None applicable — this is a scripture/art-meaning piece, not a data-driven
claim. No statistics are used in this content.

## Specific examples

- Direct scripture text (ESV), verified via WebSearch since biblegateway.com,
  biblehub.com, and esv.org are blocked by the egress proxy for direct
  fetching (search-result snippets and aggregator confirmations used
  instead — see sources.md):
  - John 4:14 (ESV): "Everyone who drinks of this water will be thirsty
    again, but whoever drinks of the water that I will give him will never
    be thirsty again. The water that I will give him will become in him a
    spring of water welling up to eternal life."
  - John 4:10 (ESV, context): "...he would have given you living water."
  - Isaiah 12:3 (ESV): "With joy you will draw water from the wells of
    salvation."

## Risks, counterarguments, or limitations

- **Don't overclaim the scripture connection.** The catalog description
  never cites John 4 or Isaiah 12 by chapter/verse — "well of living
  water" is Agata's own phrase. The post should use the verified verses as
  *resonant, real scripture that shares this image*, phrased as an
  association ("echoes," "brings to mind"), not as "this painting depicts
  John 4:14" or any claim that Agata intended a specific verse. That would
  be inventing authorial intent she hasn't stated.
- **No personal backstory available beyond the catalog text.** The
  description is written in third person about the painting's symbolism,
  not first-person from Agata about why she made it — unlike some other
  catalog entries. Per the run instructions, this post should stay
  image-led and description-led rather than inventing a personal
  narrative Agata hasn't supplied.
- **Framing detail ("white frame available... after January 4th")** is
  time-ambiguous in the source data (year not given, and the catalog
  itself is dated 2026-08-21, well past any January 4th) — omitted from
  the post as a specific claim; if frame options matter, direct people to
  the shop link rather than asserting current framing availability.
- **Price is currently accurate per catalog** (no sale, no stale-price
  flag) but should still be treated as "at last check" language rather
  than a guaranteed current price, per this pipeline's general practice
  around Squarespace price drift.

## Possible content angles

1. **The divided composition itself** — lead with the visual structure:
   burden above, renewal below, with living water as the turning point.
   Strong for all three platforms; visual and emotionally direct.
2. **Living water as an image for what only God supplies** — pair the
   painting's "well of living water" language with John 4:14's "spring of
   water welling up to eternal life," framed as an echo, not a caption.
   Strongest angle for LinkedIn/Instagram main caption — specific,
   verifiable, on-pillar (healing, faith, overcoming struggle).
3. **From darkness to light, not around it** — the journey angle: this
   painting doesn't skip the "burden" realm to get to "purity," it holds
   both in one frame, which mirrors the client's "overcoming struggles by
   staying faithful to God" pillar without erasing the struggle itself.
4. **Collector-facing angle** — a mid-priced ($750), single-edition
   Atelier piece with a clear original story, useful for an audience
   segment interested in acquiring meaningful work (secondary angle).

Angle 2 (living water, grounded in verified John 4:14 / Isaiah 12:3 text)
is the strongest for the main hook, with angle 1 (the divided composition)
as the concrete visual detail that opens the post. Angle 3 supports the
CTA/closing thought. This mirrors the same "resonant scripture + verified
text, not a misattributed caption" discipline used in post 013's research.

## Research notes

- Sourced facts: all painting details (title, price, dimensions if given,
  medium, availability, catalog description) — from painting-catalog.json
  (live Squarespace API snapshot, 2026-08-21). Scripture text — from
  WebSearch results citing ESV.org, BibleHub, Biblia (see sources.md).
- Inference/synthesis (clearly separated from the above): the connection
  between the catalog's "well of living water" phrase and John 4:14 /
  Isaiah 12:3 is this brief's own association — not asserted by Agata or
  the catalog as a specific citation. Writers must phrase this as an echo
  or resonance, never as "this painting illustrates John 4" or any claim
  about the artist's specific intent.
- No statistics or third-party examples were needed for this topic.
