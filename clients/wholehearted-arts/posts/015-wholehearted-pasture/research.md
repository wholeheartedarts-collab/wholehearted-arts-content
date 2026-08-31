# Research Brief: "Wholehearted Pasture" (Studio Collection)

**Run type:** Automated scheduled pipeline run, 2026-08-31.
**Selection rule applied:** Per `painting-catalog.json`'s `_selection_rule`, pick
from the collection with fewer entries in `used`. The catalog's own snapshot
(regenerated 2026-08-21) shows Atelier=6 used, Studio=4 used — but posts 012
("In the Cradle of Faith"), 013 ("Held by the Word"), and 014 ("Cleansing
Waters - Divided by Grace") all ran after that snapshot and are not yet
reflected in the catalog's `used` lists. Reconciling directly against the
actual `clients/wholehearted-arts/posts/` folders (same approach post 014's
own research took): real counts are Atelier=7 used (002, 003, 004, 007, 009,
011, 014), Studio=6 used (005, 006, 008, 010, 012, 013). Studio has fewer —
not a tie, so the tiebreaker wasn't needed. Both "In the Cradle of Faith" and
"Held by the Word" were excluded from this run's candidate pool since they're
already covered, verified directly against posts 012 and 013's own files.
**Painting/product details source:** `clients/wholehearted-arts/painting-catalog.json`,
regenerated 2026-08-21 directly from the live Squarespace Commerce API.
**Egress note:** A single WebFetch to www.wholeheartedarts.com was tested this
run and returned `EGRESS_BLOCKED`. Per instructions, not retried — all painting
facts below come from the catalog (itself live API data, not a stale scrape).

## Painting details (from catalog, studio.unused)

- **Title:** Wholehearted Pasture
- **Collection:** Studio Collection ("Modern Christian Art")
- **Price:** $125.00 USD — no `sale_price`, no `price_note`. Current as of the
  2026-08-21 catalog snapshot; no discrepancy to flag.
- **Availability:** "1 in stock" — no `availability_note`. No concern.
- **Medium:** Mixed media — fabric and acrylic.
- **Dimensions:** 8" x 10".
- **Product URL:** https://www.wholeheartedarts.com/studio-collection-agata-christian-art/p/xglk8pegygsyvvdt1mc22ddw2of9u3
  (not verified live this run — egress blocked; taken from catalog).
- **Image URL:** https://images.squarespace-cdn.com/content/v1/5b412dba5ffd201a3f9205e4/1680747884654-50WSR14DD9XC90CEFO5X/86452606-61A1-470A-88AD-233F2BB32783
- **Catalog description (verbatim, complete):** "Mixed Media / Fabric and
  Acrylic / John 13:5 scripture written into the Sky / Size 8"/10""
- **No `caution_note` on this entry.**

## Executive summary

"Wholehearted Pasture" is a small (8"x10") mixed-media piece with John 13:5 —
the verse describing Jesus pouring water into a basin to wash the disciples'
feet — written into its sky. The catalog gives no narrative beyond the
scripture reference and materials: no story of what prompted the piece, no
description of its visual composition beyond "sky." This is a genuinely
thin-narrative entry per the catalog's own skip_rules guidance ("for
thin-narrative pieces keep the post shorter and image-led rather than
inventing backstory"), so this topic's posts should stay short, image-led,
and let the scripture and the painting's title (which directly echoes the
brand name "WholeheartedArts") carry the content rather than inventing a
studio story that isn't in the record.

## Key points

- The verse is specific and verifiable: John 13:5 describes Jesus, at the
  Last Supper, taking the posture of a servant to wash his disciples' feet —
  a task normally done by the lowest household servant.
  - John 13:5 (ESV): "Then he poured water into a basin and began to wash the
    disciples' feet and to wipe them with the towel that was wrapped around
    him."
- The wider passage (John 13:12-17) makes the meaning explicit: Jesus
  presents the foot-washing as a deliberate example of humble service for
  his followers to imitate, not just a one-off act of kindness.
  - John 13:14 (ESV): "If I then, your Lord and Teacher, have washed your
    feet, you also ought to wash one another's feet."
  - John 13:15 (ESV): "For I have given you an example, that you also should
    do just as I have done to you."
- The painting's title doubles as a natural, unforced echo of the brand name
  ("Wholehearted" / "WholeheartedArts") — a real, present coincidence in the
  catalog data, not something invented for the post.
- "Pasture" in the title is not glossed by the catalog at all — there is no
  shepherd/Psalm 23 language in the description, only "John 13:5... written
  into the Sky." Content should not assume or invent a shepherd/pasture
  scripture connection that the catalog doesn't support; if the word
  "pasture" is referenced, it should be treated as the artist's own title
  choice, not explained with invented meaning.

## Notable statistics

None applicable — this is a scripture/art-meaning piece, not a data-driven
claim.

## Specific examples

- Direct scripture text (ESV), verified via WebSearch since biblegateway.com,
  biblehub.com, and esv.org are blocked by the egress proxy for direct
  fetching (search-result snippets from those same sites were used instead —
  see sources.md):
  - John 13:5 (ESV): "Then he poured water into a basin and began to wash the
    disciples' feet and to wipe them with the towel that was wrapped around
    him."
  - John 13:14 (ESV): "If I then, your Lord and Teacher, have washed your
    feet, you also ought to wash one another's feet."
  - John 13:15 (ESV): "For I have given you an example, that you also should
    do just as I have done to you."

## Risks, counterarguments, or limitations

- **Thin source material.** The catalog description is four lines of
  materials/scripture citation only — there is no artist statement about why
  this piece was made, what "pasture" refers to visually, or what the sky
  looks like. Writers must not invent a studio story, a personal anecdote, or
  a visual description of the painting beyond what a viewer could plausibly
  see in the final image. Keep copy short and let the image do the work.
- **Do not conflate this verse with Psalm 23 shepherd/pasture imagery.** The
  word "pasture" in the title invites an easy (but unsupported) leap to "The
  Lord is my shepherd... he makes me lie down in green pastures" (Psalm
  23:1-2). The catalog gives no indication this painting references Psalm 23
  — only John 13:5 is cited. Any post using this painting must stick to John
  13 (service, humility, foot-washing) and not silently import Psalm 23
  imagery the artist never claimed.
- **Small, low-price piece.** At $125 and 8"x10", this reads as an
  accessible/entry-point piece rather than a statement work — content should
  not oversell it as monumental; a quieter, humbler framing actually fits
  both the piece's size and its subject (humility/service).

## Possible content angles

1. **Service as the posture, not the size.** Jesus took a towel and a basin
   — the lowest task in the house — and made it the clearest picture of
   love in the whole Gospel. A small painting carrying a small, quiet act.
2. **"Wholehearted" as a two-way echo.** The painting's own title lands on
   the same word as the studio's name — not a tagline, just what showing up
   with a towel and basin actually looks like.
3. **An example to follow, not just admire.** John 13:15 turns the
   foot-washing from a story about Jesus into an instruction for everyone
   watching — this piece as a quiet, physical reminder to actually do it.
4. **Image-led, minimal copy.** Given the thin narrative, a short caption
   that names the verse, states plainly what's in the sky, and lets the
   piece speak — appropriate especially for Instagram.

## Research notes

- All scripture verification done via WebSearch (search-result snippets from
  ESV.org, Biblia, Bible.com, BibleHub — direct fetch to those domains is
  blocked by the egress proxy per this environment's known restrictions).
  Exact wording confirmed and quoted verbatim above; nothing paraphrased as if
  it were a direct quote.
- No claims in this brief are inferred beyond what is directly stated in
  either the catalog entry or the verified scripture text. Any interpretive
  language ("small, quiet act," "quieter, humbler framing") is flagged here
  as this pipeline's own synthesis, not an artist statement, so writers know
  it's a proposed angle rather than a documented fact.
