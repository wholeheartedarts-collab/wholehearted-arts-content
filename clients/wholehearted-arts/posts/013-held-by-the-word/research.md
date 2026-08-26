# Research Brief: "Held by the Word- Be Still and Know that I am God" (Studio Collection)

**Run type:** Automated scheduled pipeline run, 2026-08-26.
**Selection rule applied:** Per `painting-catalog.json`'s `_selection_rule`, pick
from the collection with fewer entries in `used`. The catalog itself (regenerated
2026-08-21) shows Atelier=6 used, Studio=4 used — but post 012
("In the Cradle of Faith," a Studio painting) ran 2026-08-24, after the catalog
snapshot, and is not yet reflected in the catalog's `used` list. Accounting for
that undocumented pick, the real counts are Atelier=6, Studio=5. Studio still
has fewer used entries, so the rule still points to Studio — not a tie, so the
tiebreaker wasn't needed. "In the Cradle of Faith" was excluded from this run's
candidate pool since it's already covered (verified directly against post
012's own files, not just the catalog).
**Painting/product details source:** `clients/wholehearted-arts/painting-catalog.json`,
regenerated 2026-08-21 directly from the live Squarespace Commerce API.
**Egress note:** A single WebFetch to www.wholeheartedarts.com was tested this
run and returned `EGRESS_BLOCKED`. Per instructions, not retried — all painting
facts below come from the catalog (itself live API data, not a stale scrape).

## Painting details (from catalog, studio.unused)

- **Title:** Held by the Word- Be Still and Know that I am God
- **Collection:** Studio Collection ("Modern Christian Art")
- **Price:** $650.00 USD, **sale price $350.00 USD** — `price_note`: "ON SALE
  at time of snapshot — verify before quoting any price in a post." Flagged
  for Agata in the Step 13 email; this post will not state a price as settled
  fact.
- **Availability:** 1 in stock — no availability concern.
- **Medium:** Mixed media — fabric/acrylic painting.
- **Dimensions:** 10" x 20", unframed.
- **Product URL:** https://www.wholeheartedarts.com/studio-collection-agata-christian-art/p/0e38znyhddoda8nnlvmodbwphmvi7z
  (not verified live this run — egress blocked; taken from catalog).
- **Image URL:** https://images.squarespace-cdn.com/content/v1/5b412dba5ffd201a3f9205e4/1677101676936-FJ01UXROA3KDNY5GD27E/C9D6166C-1ECE-4FB1-B128-B24DF5581722
- **Catalog description (verbatim):** "There is something so beautiful to me
  about truth being hidden in plain sight. This original 10" x 20" mixed
  media painting holds layers of color, texture, movement, and softness, but
  also something deeper: scripture from Psalm 37 woven into the background.
  That matters to me. Because the Word of God is not just something we read
  and move on from. It becomes the background of how we live. How we endure.
  How we hope. How we stay steady. She feels reflective, peaceful, almost
  wrapped in that truth. Not untouched by life, but held through it. This is
  a one-of-a-kind original created for someone who wants art with beauty,
  meaning, and spiritual depth."
- **No `caution_note` on this entry.**

## Executive summary

"Held by the Word" pairs a title that echoes the well-known "be still and
know" language with a catalog description that specifically credits Psalm 37
— not Psalm 46 (the more famous source of "Be still, and know that I am
God," v.10). Verification below confirms this isn't an error: Psalm 37:7
independently contains near-identical "be still" language ("Be still before
the LORD and wait patiently for him"), so the title and the Psalm 37
attribution are both defensible without conflating the two psalms. The piece
fits squarely in the client's faith/emotion/healing content pillar: scripture
as something lived with rather than just read, steadiness formed through
waiting.

## Key points

- The painting's own description frames scripture not as decoration but as
  something structural — "the background of how we live" — a specific,
  quotable framing already supplied by the artist via the catalog, not
  invented by this pipeline.
- Psalm 37 as a whole is about trusting God's timing during seasons that
  test patience: don't fret over others "who prosper," commit your way to
  the Lord, and — the verse most relevant here — be still and wait.
- There is a real, common point of confusion: "Be still, and know that I am
  God" (the very famous version of this phrase) is Psalm 46:10, not Psalm
  37. This post must not attribute the Psalm 46:10 wording to Psalm 37. It
  should instead reference Psalm 37:7's own "be still ... and wait
  patiently" language, which is different wording carrying a similar spirit.

## Notable statistics

None applicable to this topic — this is a scripture/art-meaning piece, not a
data-driven claim. No statistics are used in this content.

## Specific examples

- Direct scripture text (ESV), verified via WebSearch since biblegateway.com,
  biblehub.com, and esv.org are blocked by the egress proxy for direct
  fetching (search-result snippets from those same sites, and others, were
  used instead — see sources.md):
  - Psalm 37:7 (ESV): "Be still before the LORD and wait patiently for him;
    fret not yourself over the one who prospers in his way, over the man who
    carries out evil devices!"
  - Psalm 37:5 (ESV): "Commit your way to the LORD; trust in him, and he
    will act."
  - Psalm 37:3-4 (ESV): "Trust in the LORD, and do good; dwell in the land
    and befriend faithfulness. Delight yourself in the LORD, and he will
    give you the desires of your heart."

## Risks, counterarguments, or limitations

- **Scripture attribution risk (addressed above):** the temptation is to
  quote the famous "Be still, and know that I am God" (Psalm 46:10) since
  it's in the painting's title, then casually cite "Psalm 37" underneath it
  — that would misattribute a Psalm 46 verse to Psalm 37. Writers for this
  topic must use Psalm 37:7's own wording ("be still ... and wait
  patiently") if quoting scripture, and should not present Psalm 46:10's
  exact phrase as if it's what's written in the piece, since the catalog
  only claims Psalm 37 is woven into the background.
- **Price is not settled** — sale price note above. Posts should avoid
  stating a specific price as a hard, current fact; if a price is mentioned
  at all, it should be framed as "at last check" or simply omitted in favor
  of directing people to the shop link.
- **No personal backstory beyond the catalog text is available** — Agata's
  description already supplies a first-person reflection ("There is
  something so beautiful to me...That matters to me"), which is usable
  verbatim/paraphrased since it's her own words in the product listing. No
  additional invented backstory should be added.

## Possible content angles

1. **Scripture as structure, not decoration** — lead with the catalog's own
   line: art (and life) built with something deeper "woven into the
   background," using Psalm 37:7's actual wording.
2. **The waiting angle** — Psalm 37 is fundamentally about the discipline of
   waiting on God's timing without fretting over others who seem to be
   getting ahead; pair with the painting's soft, layered, "held through it"
   visual description.
3. **"Held" as the operative word** — the title's use of "held" (not
   "solved," not "fixed") as the emotional core: faith as something that
   carries you through, not something that removes the difficulty.
4. **Studio Collection accessibility angle** — this piece is more modestly
   sized/priced than some Atelier statement pieces, useful for a
   collector-audience post about starting or growing a meaningful
   collection (secondary angle, not primary).

Angle 2 (the waiting angle, grounded in verified Psalm 37:7 text) is the
strongest for LinkedIn/Instagram/Facebook: it's specific, verifiable, and
matches the client's pillar of "overcoming struggles by staying faithful to
God" without inventing anything beyond the catalog + verified scripture.

## Research notes

- Sourced facts: all painting details (title, price, dimensions, medium,
  availability, catalog description) — from painting-catalog.json (live
  Squarespace API snapshot, 2026-08-21). Scripture text — from WebSearch
  results citing ESV.org, BibleHub, Biblia, YouVersion (see sources.md).
- Inference/synthesis (clearly separated from the above): the observation
  that the title echoes Psalm 46:10 while the description cites Psalm 37,
  and the resolution that Psalm 37:7 independently supports "be still"
  language, is this brief's own analysis — not asserted by Agata or the
  catalog. Writers should treat this as helpful context to avoid a
  misattribution error, not as a fact to state explicitly in the post
  itself (no need to give the audience a scripture-citation lecture).
- No statistics or third-party examples were needed for this topic.
