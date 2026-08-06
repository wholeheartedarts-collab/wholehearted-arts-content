---
name: accessibility-alt-text
description: Write accurate, accessible alt text for a post's final chosen image. Use right after image-generation produces a final image, before content-package-review.
---

# Accessibility Alt Text

## Purpose

Describe the meaningful visual content of the final image for someone who
cannot see it. Accuracy and accessibility take priority over hitting any
specific length target.

## Process

1. Look at the final chosen image (not earlier discarded versions).
2. Describe what's actually depicted: subject, setting, notable visual
   details, mood/tone if visually evident, any text rendered in the image.
3. Do not describe the post's message or restate the caption — describe
   the image itself.
4. Keep it accurate and specific rather than generic ("a colorful abstract
   painting with swirling blue and gold brushstrokes" beats "an artistic
   image"). A detailed description (roughly 500 characters) is a
   reasonable target, but never pad it just to hit a length.

## Output

For a single-platform topic (the existing convention), save
`clients/[client-slug]/posts/[NNN-topic-slug]/alt-text.md`:

```
Image: images/v[N].png
Alt text: [final alt text]
```

For a multi-platform topic, each platform's image gets its own alt text
file (since platforms may use different crops of the same image, or
entirely different images) — save
`clients/[client-slug]/posts/[NNN-topic-slug]/alt-text/[platform].md`
using the same format, one file per platform actually produced.

## Hard rule

Alt text must match the actual final image and the actual post — verify
both before finalizing. If the image is later regenerated as a new
version, alt text must be rewritten for that version, not reused. This
applies per platform — a new Instagram crop needs its own alt-text
rewrite even if the LinkedIn version is unchanged.
