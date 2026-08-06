---
name: publishing-handoff
description: Manage the draft/approved/scheduled/published status of a content package and hand off for manual publishing. Use only after content-package-review passes and the human has given explicit approval — never to auto-publish.
---

# Publishing Handoff

## Status model

Every package has a `status.json` in its topic folder with one of these
states, tracked as distinct and never skipped:

```json
{ "status": "draft", "history": [...] }
```

- `draft` — in progress, not yet review-passed.
- `review-ready` — passed [[content-package-review]] (or passed with
  clearly flagged NEEDS HUMAN DECISION items), awaiting human approval.
- `approved` — human has explicitly approved the content as-is.
- `scheduled` — human has given a specific date/time to publish.
- `published` — actually posted (recorded after the human confirms it
  went live, since this system does not auto-post to LinkedIn).

## Hard rules

- Never move a package (or a specific platform within a package) to
  `approved`, `scheduled`, or `published` without an explicit human
  instruction naming that exact package/platform.
- Never auto-publish or auto-schedule via browser bots or scraping,
  ever, for any platform. This client's accounts are real accounts she
  operates — do not use automation that risks them being flagged.
- Default to a **human-led manual publishing workflow**: present the
  final text, image, and alt text so the human can copy/paste and post
  it themselves. This remains the default and the fallback for any
  platform not connected through the sanctioned path below.
- An **officially supported, explicitly authorized API integration** may
  be used instead of manual posting — this is not a workaround of the
  rule above, it's the exception the rule always allowed. As of
  2026-08-06, this client has authorized exactly one such integration:
  **Buffer**, connected via its official hosted MCP server
  (`mcp.buffer.com/mcp`) with Agata's own OAuth login, covering her
  LinkedIn, Instagram Business, and Facebook Page accounts (all
  confirmed in `profile.md`). No other automation is authorized.

## Buffer-connected path (per platform, per package)

1. Applies only after a specific package/platform has reached `approved`
   with a date/time (i.e. `scheduled`) via explicit human instruction —
   Buffer is a delivery mechanism for a decision already made, never a
   new approval path of its own.
2. Confirm Buffer's MCP tools are connected and that the target
   platform's account is linked in Buffer before attempting this path —
   if not connected, fall back to the manual path for that platform
   without blocking the other platforms.
3. Create a **scheduled** (not immediately-published) update in Buffer
   for that platform, using the final approved text, image, and the
   given date/time.
4. Record in `status.json` under that platform's entry: which method was
   used (`"scheduled_via": "buffer"` or `"manual"`) and Buffer's own
   scheduled time, so the record reflects what was actually queued.
5. Never use Buffer (or any integration) to *publish immediately* on a
   human's approval alone — approval without a specific date/time means
   `approved`, not `scheduled`; only schedule when a date/time was given.

### First-time connection safety check

The first time Buffer is used for this client, create one **draft,
unscheduled** test update (not published, not even scheduled) to confirm
the connection and tool calls work correctly before trusting it with any
real content. Discard the test update afterward.

## On approval

1. Update `status.json` to `approved` (or `scheduled` with a date/time if
   given) — per platform, since platforms can be at different stages for
   the same topic (see [[content-package-review]] folder convention for
   multi-platform topics).
2. Preserve a final copy of: post text, image file reference, alt text,
   intended date/platform, delivery method (manual or Buffer), and
   status — this is the record of what was actually approved, even if
   the live post is later edited.

## Never

- Edit or delete a live post without explicit authorization.
- Silently republish a package that was previously rejected — treat
  revisions as a new version with its own history entry, not a status
  overwrite.
