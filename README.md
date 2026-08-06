# WholeheartedArts — Multi-Platform Content System

A repeatable, file-based pipeline for producing research-backed,
brand-consistent social content across **LinkedIn, Instagram, and
Facebook**: research → write → review → image → alt text → final review
→ human approval → (optional) Buffer draft. Nothing publishes or
schedules automatically — every package stops for explicit human
approval.

Built from the process described in `AIAP C12 | Bonus Live Session 2`
(see the transcript PDF, kept locally, gitignored). Started 2026-07-19 as
LinkedIn-only; expanded 2026-08-06 to add Instagram, Facebook, Buffer
scheduling, and a scheduled cloud automation routine.

## How it works

`CLAUDE.md` is the orchestrator — it defines the per-platform workflow
and points to the specialized skills in `.claude/skills/`: research,
brand-voice, linkedin/instagram/facebook-writing, linkedin/instagram/
facebook-review, factual-verification, visual-style, image-generation,
accessibility-alt-text, content-package-review, publishing-handoff,
performance-learning, client-profile.

## Setup

1. **Credentials**: copy `.env.example` to `.env` and fill in
   `GEMINI_API_KEY` (used by image-generation when a piece needs an
   AI-generated image rather than a real sourced photo). Never paste the
   key into chat. `.env` is gitignored.
2. **Buffer**: connected via its official hosted MCP server
   (`mcp.buffer.com/mcp`), OAuth-authorized to Agata's own Buffer account
   — covers LinkedIn (personal profile), Instagram (Business), and the
   WholeheartedArts Facebook Page. Buffer is the only sanctioned
   auto-posting path, and even then only for **drafts** by default —
   scheduling/publishing still requires an explicit human instruction
   naming the exact package, platform, and date/time.
3. **Client profile**: `clients/wholehearted-arts/profile/profile.md` —
   edit directly, or ask the agent to update it.
4. **Brand voice**: currently provisional. Give the agent real posts,
   articles, or book excerpts and ask it to re-run [[brand-voice]].
5. **Visual style**: `clients/wholehearted-arts/visual-style/
   style-guide.json` — still a placeholder pending real reference images,
   but already has a per-platform `dimensions` map in use.

## Folder structure

```
CLAUDE.md                        orchestrator — start here
.claude/skills/                  one skill per concern
clients/wholehearted-arts/
  profile/profile.md             client config
  profile/brand-voice.md
  visual-style/style-guide.json
  posts/
    NNN-topic-slug/
      research.md, sources.md, fact-check.md      shared across platforms
      linkedin-post.md, linkedin-review.md
      instagram-post.md, instagram-review.md
      facebook-post.md, facebook-review.md
      package-review.md          final gate, covers every platform variant
      status.json                per-platform status + Buffer draft IDs
      images/, alt-text/         per platform
```

Posts `001` and `002` predate the multi-platform convention and use the
older flat, LinkedIn-only layout — not migrated, kept as-is.

## Running a new topic (manual, in chat)

Give the agent a prompt like:

> Create the next numbered content package. Topic: "[TOPIC]". Any
> specific facts, angle, or real work (painting, book) to build it
> around.

It runs research → brand-voice check → write → platform review →
fact-check → image → alt text → full package review across whichever
platforms the topic targets, saves everything under the next numbered
`posts/NNN-topic-slug/` folder, and **stops** to present the package.

## Automated pipeline (scheduled cloud routine)

A scheduled Claude Code cloud routine, **"WholeheartedArts Content
Pipeline"** (Mon/Wed/Fri, 8:00 AM America/New_York — manage it at
https://claude.ai/code/routines), runs the same pipeline unattended: picks
an unused real painting from wholeheartedarts.com, researches its theme,
writes and reviews all three platforms, sources the real photo, fact-checks
everything, and lands three **unscheduled draft posts in Buffer** — never
auto-approves or schedules. Review and approve/schedule from inside Buffer
itself, or come back to chat with change requests.

This routine runs against a **public** GitHub mirror of this repo
(`github.com/wholeheartedarts-collab/wholehearted-arts-content` — public
because private-repo access for cloud routines needs a Claude Team/
Enterprise plan; no secrets are in the repo, `.env` stays local and
gitignored). Push local changes to `origin main` so the next scheduled run
sees them.

## Approving and publishing

Nothing moves past `review-ready` without an explicit human instruction.
Two paths from there:
- **Manual**: copy the final text/image/alt text and post it yourself.
- **Buffer**: ask the agent to create a draft (or, once you give an exact
  date/time, a scheduled post) via the Buffer MCP connection. Even
  through Buffer, nothing is scheduled without you naming the exact
  package, platform, and time.

## Adding a new client

Ask the agent to onboard a new client — it will create
`clients/[new-slug]/` with the same structure and walk through the intake
fields in `.claude/skills/client-profile/SKILL.md`.

## What this system will not do

- Fabricate sources, statistics, quotes, or personal stories.
- Generate an image before the post text is finalized, or before a real
  sourced photo has been ruled out for a real, existing artwork.
- Auto-approve, auto-schedule, or auto-publish anything, or edit/delete a
  live post, without explicit authorization naming the exact package.
- Ask you to paste API keys into chat.


