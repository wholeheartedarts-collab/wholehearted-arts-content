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
  confirmed in `profile.md`). No other automation is authorized. Since
  2026-09-30 only LinkedIn and Instagram are staged — Instagram
  cross-posts to the Facebook Page.

## Buffer staging rules — corrected 2026-09-30 (read before using Buffer at all)

**Verified by direct test on 2026-09-30, on all three channels:**
`create_post` with `schedulingType: "automatic"`, `saveToDraft: true`,
`mode: "addToQueue"` and no `dueAt` produces a genuinely inert Buffer
**draft** — `status: "draft"`, `dueAt: null`, `sentAt: null`,
`sharedNow: false`. It sits in the channel's **Drafts** tab until a human
opens it and chooses "Add to Queue" or "Share Now". LinkedIn and Facebook
test drafts were created, re-read, and deleted without ever entering the
queue.

### What actually went wrong before (root cause, corrected)

- **The August 2026 "auto-publish bug" was a misdiagnosis.** Posts 003 and
  004 show `sharedNow: true` in Buffer — they were published by a
  **Share Now** action taken on the drafts in Buffer's UI minutes after
  creation, not by `saveToDraft` being ignored. The drafts themselves were
  real drafts.
- **The fix built on that misdiagnosis broke the pipeline for two months.**
  Instagram drafts were created with `schedulingType: "notification"`,
  which is Buffer's **Reminder** mode: Buffer never publishes the post
  itself, it only sends a push notification to the Buffer *mobile app*,
  and the human finishes the post on their phone. Agata does not use the
  mobile app, so every attempt to publish from the web either errored
  ("trouble sending notifications to your mobile device") or silently
  consumed the draft. Meanwhile LinkedIn/Facebook were parked on Buffer's
  **Ideas** board, which is not the Drafts tab and which Agata never saw.
  Net effect: "I only get Instagram drafts, and they won't post."
- On 2026-09-30 every existing Instagram draft was switched to
  `automatic`, every LinkedIn idea was converted to a real draft, and the
  cloud routine prompt was rewritten to match this section.

### The rules

- **Every Buffer `create_post` is:** `schedulingType: "automatic"`,
  `saveToDraft: true`, `mode: "addToQueue"`, no `dueAt`. Instagram also
  needs `metadata.instagram: { type: "post", shouldShareToFeed: true }`.
- **Never `schedulingType: "notification"`** — that is Reminder mode and
  requires the phone app.
- **Never `mode: "shareNow" | "shareNext" | "customScheduled"` and never
  pass `dueAt`** unless a human has explicitly approved that exact
  package and named the time. Those actions publish or schedule for real.
- **Never `create_idea`** for staging. Ideas are not drafts and are not
  where Agata looks.
- **After every `create_post`, immediately `get_post` the returned ID**
  and confirm `status: "draft"`, `dueAt: null`, `sentAt: null`,
  `sharedNow: false`, `schedulingType: "automatic"`. If it is anything
  else, `delete_post` it at once and report loudly.
- **Platforms:** LinkedIn and Instagram only. Agata's Instagram account
  cross-posts to her Facebook Page, so no separate Facebook post is
  written or staged (her decision, 2026-09-30). Do not create anything on
  the Facebook channel.
- **Publishing is Agata's action, in Buffer's own UI**: open the draft in
  the Drafts tab and choose "Add to Queue" (next slot on the channel's
  posting schedule) or "Share Now". No phone app is involved. Remember
  that "Share Now" really does post immediately — that is what published
  003 and 004.

## Buffer-connected path (per platform, per package)

1. Applies only after a specific package/platform has reached `approved`
   with a date/time (i.e. `scheduled`) via explicit human instruction —
   Buffer is a delivery mechanism for a decision already made, never a
   new approval path of its own. **Exception**: LinkedIn and Instagram
   are pushed at `review-ready` as real, unscheduled Buffer **drafts**
   per the staging rules above — genuinely inert until Agata acts on them
   in Buffer's Drafts tab.
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
6. **After every Buffer `create_post` call, immediately `get_post` the
   returned ID and check `status`/`dueAt`/`sentAt`.** Do not assume
   `saveToDraft` or `schedulingType` did what was requested — verify.
   This step is mandatory precisely because it was skipped on
   2026-08-06 and 2026-08-09/10, and both times the post had already
   gone live for real without anyone noticing until much later.

### First-time connection safety check

The first time Buffer is used for this client, create one **draft,
unscheduled** test update (not published, not even scheduled) to confirm
the connection and tool calls work correctly before trusting it with any
real content. Discard the test update afterward. **Immediately verify
with `get_post`** that it actually stayed a draft (per the limitation
above) — do not just assume it worked because the call returned
success.

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
