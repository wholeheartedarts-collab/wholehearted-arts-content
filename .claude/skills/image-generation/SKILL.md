---
name: image-generation
description: Generate an image (LinkedIn, Instagram, and/or Facebook) for a finished, reviewed post. Use only after that platform's writing and review skills are complete — never before or independently of the post text.
---

# Image Generation

## Prerequisites (strict order)

1. The finished post for the **target platform** (`linkedin-post.md`,
   `instagram-post.md`, or `facebook-post.md`) exists and has passed that
   platform's review skill.
2. `clients/[client-slug]/visual-style/style-guide.json` has been loaded
   (see [[visual-style]] — placeholder is acceptable if no references
   exist yet), specifically its `dimensions` map for the target platform.

Never generate an image from the topic alone — always read the finished
post first so the image supports its actual message, hook, and tone. If
a topic targets multiple platforms, generate/export one image per
platform rather than assuming one crop works everywhere — LinkedIn,
Instagram, and Facebook have different native dimensions (see below).

## Provider

This project is wired for **Google Gemini / Imagen**. The API key is
never pasted into chat or written into any file in this repo.

- Read it from the environment variable `GEMINI_API_KEY`.
- If it's not set, stop and tell the human to set it (see
  `.env.example` at the project root) — do not ask them to paste it, and
  do not proceed with a placeholder image silently.

## Generating the image

1. Summarize the target platform post's core message and hook in a few
   lines.
2. Combine that with `style-guide.json` to build the image prompt:
   subject relevant to the actual post content, composition/palette/mood
   from the style guide, dimensions from `style-guide.json`'s
   `dimensions` map for the target platform (e.g. `dimensions.linkedin`,
   `dimensions.instagram_feed`, `dimensions.facebook`).
3. Generate the image via the Gemini/Imagen API using `GEMINI_API_KEY`
   from the environment.
4. Save to
   `clients/[client-slug]/posts/[NNN-topic-slug]/images/[platform]-v1.png`
   (or the appropriate next version number — see below). For a
   single-platform topic (still the common case for LinkedIn-only work),
   the existing unprefixed `images/v1.png` convention is unchanged.

## Using a real (non-generated) image instead

If the human explicitly wants an actual real photo used instead of a
generated image (e.g., a real photo of the client's own artwork, as with
post 002's "Fear Not" painting), skip Gemini generation entirely for that
image. Note the deviation explicitly in `status.json` and `review.md` —
this is a valid, human-directed path, not a shortcut around the skill.
When the same real photo needs to serve multiple platforms, export a
separate crop per platform's dimensions rather than reusing one crop
everywhere — a LinkedIn landscape crop and an Instagram portrait crop of
the same source photo are two different files.

## Versioning rule

**Never overwrite an existing image.** If regenerating (new style guide,
revision after feedback), save as `[platform-]v2.png`, `[platform-]v3.png`,
etc. in the same `images/` folder so a human can compare versions side by
side. Record which version is the current pick per platform in
`status.json`.

## Consistency

Images across posts for the same client should feel like one coherent
family (same style-guide application), while remaining specific to each
post's actual content — never a generic template image reused
unmodified.

## After generation

Hand off to [[accessibility-alt-text]] to write alt text for the final
chosen image before the package goes to [[content-package-review]].
