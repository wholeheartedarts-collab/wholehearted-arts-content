# Wholehearted Arts — LinkedIn Content System

A repeatable, file-based pipeline for producing research-backed,
brand-consistent LinkedIn content: research → write → review → image →
alt text → final review → human approval. Nothing publishes
automatically.

Built from the process described in `AIAP C12 | Bonus Live Session 2`
(see the transcript PDF and `outputs/social-media-agency-master-prompt.md`
this was generated from). Currently scoped to LinkedIn only; the
structure supports adding other platforms later without disturbing this
one.

## How it works

`CLAUDE.md` is the orchestrator — it defines the workflow and points to
the specialized skills in `.claude/skills/`. Each skill is a focused,
independently testable set of instructions (research, brand-voice,
linkedin-writing, linkedin-review, factual-verification, visual-style,
image-generation, accessibility-alt-text, content-package-review,
publishing-handoff, performance-learning, client-profile).

## Setup

1. **Credentials**: copy `.env.example` to `.env` and fill in
   `GEMINI_API_KEY` (used by the image-generation skill for Google
   Gemini/Imagen). Never paste the key into chat — the agent will only
   ever read it from the environment. `.env` is gitignored.
2. **Client profile**: `clients/wholehearted-arts/profile/profile.md` is
   already set up with provisional details. Edit it directly, or just
   tell the agent what to change and ask it to update the file.
3. **Brand voice**: currently provisional (built from the profile
   config, not real samples). When you have LinkedIn posts, articles, or
   book excerpts to share, give them to the agent and ask it to re-run
   [[brand-voice]] — it'll replace the provisional guide.
4. **Visual style**: no reference images yet, so image-generation uses a
   minimal placeholder style guide
   (`clients/wholehearted-arts/visual-style/style-guide.json`). When you
   have 3-6 images that capture the look you want, give them to the agent
   and ask it to build the real style guide via [[visual-style]].

## Folder structure

```
CLAUDE.md                        orchestrator — start here
.claude/skills/                  one skill per concern
clients/wholehearted-arts/
  profile/profile.md             client config + (eventually) brand-voice.md
  brand-assets/                  logos, existing photos, etc.
  visual-style/style-guide.json
  performance-log.md             appears once metrics are logged
  posts/
    001-topic-slug/
      research.md
      sources.md
      linkedin-post.md
      review.md
      alt-text.md
      status.json
      images/v1.png, v2.png, ...
```

## Running a new topic

Give the agent a prompt like:

> Create the next numbered content package. Topic: "[TOPIC]". Audience:
> [art collectors / automation businesses]. Any specific examples, facts,
> or angle you want included, and any risks/counterarguments to address.

It will run research → brand-voice check → write → platform review →
fact-check → image → alt text → full package review, save everything
under the next numbered `posts/NNN-topic-slug/` folder, and **stop** to
present the package. It will not publish or schedule anything on its own.

## Approving and publishing

Nothing moves past `review-ready` status without you explicitly saying
so. When you approve a package, say so explicitly (e.g., "approve
002-topic-slug") — the agent will update `status.json` accordingly. This
system defaults to **manual publishing**: it prepares the final text,
image, and alt text for you to copy/paste and post yourself, because
automated LinkedIn posting risks account flags on a personal profile.

## Adding a new client

Ask the agent to onboard a new client — it will create
`clients/[new-slug]/` with the same structure and walk through the intake
fields in `.claude/skills/client-profile/SKILL.md`.

## Updating platform guidance

LinkedIn's format norms and best practices change over time. Periodically
(or when a post underperforms unexpectedly), ask the agent to re-research
current LinkedIn guidance and successful creators, and update
`.claude/skills/linkedin-writing/SKILL.md` accordingly.

## What this system will not do

- Fabricate sources, statistics, quotes, or personal stories.
- Generate an image before the post text is finalized.
- Auto-publish, auto-schedule, or edit/delete a live post without
  explicit authorization.
- Ask you to paste API keys into chat.


