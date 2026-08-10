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

## ⚠ Critical Buffer limitation — confirmed 2026-08-10 (read before using Buffer at all)

`saveToDraft: true` does **not** reliably keep a post inert on this
account. Root-caused after two real incidents (post 003 on 2026-08-06,
and post 004 on 2026-08-09/10 — both auto-published to LinkedIn,
Instagram, and Facebook within ~2-10 minutes of creation despite
`saveToDraft: true`, without any human approval):

- Buffer's `schedulingType` only has two values: `automatic` and
  `notification`. `notification` is the one that produces a genuinely
  inert `draft` status (confirmed via direct test). `automatic` means
  "publish for real the moment a queue slot opens" — and with
  `mode: addToQueue` (the default), that's usually within minutes,
  since channels have posting-schedule slots throughout the day.
  `saveToDraft: true` does **not** override this for `automatic`
  scheduling — that combination is not a safe "draft," it's a
  near-immediate publish.
- **Instagram** channel accepts `schedulingType: "notification"` — use
  this (with `saveToDraft: true`) for a real Instagram draft. Confirmed
  working: status stays `draft`, `dueAt`/`sentAt` stay `null`, nothing
  goes out until a human acts on it in Buffer.
- **LinkedIn and Facebook channels reject `"notification"` outright**
  ("Notification scheduling is not supported for linkedin/facebook
  channels. Use automatic scheduling instead.") — so the one
  schedulingType they accept is exactly the one that auto-publishes.
- The lower-level GraphQL `needsApproval` field (not exposed by the
  simplified `create_post` tool) looked like a possible fix but is
  blocked on this account: "needsApproval is only valid when your
  posting policy on this channel requires approval" — this org's plan
  has no approval-required posting policy configured.
- **Conclusion: there is currently no way to stage an inert,
  human-review-before-publish draft for LinkedIn or Facebook through
  Buffer's API on this account.** Only Instagram supports it.

### Practical rule this implies

- **Instagram**: safe to push to Buffer as a real draft
  (`schedulingType: "notification"`, `saveToDraft: true`) at
  `review-ready`, same as before — a human still has to act on it in
  Buffer before it posts.
- **LinkedIn and Facebook**: do **not** call Buffer's `create_post` for
  these two channels until a human has *already* given explicit
  approval to publish that exact content *right now* (or at Buffer's
  next queue slot) — there is no safe staging step for them via this
  API. Until then, hand the human the finished text + image directly
  (chat, or a file) for manual copy/paste into Buffer's own web
  composer (which may have a real "save as draft" the API doesn't
  expose) or straight into LinkedIn/Facebook. Treat any LinkedIn/
  Facebook Buffer `create_post` call as equivalent to
  publish-imminently, and get explicit per-platform approval first,
  exactly as the "Never auto-publish" hard rule already requires.
- If Buffer ever adds real approval-policy support to this account, or
  a `saveToDraft` fix ships, re-test with one throwaway post per
  channel (check `status`/`dueAt`/`sentAt` immediately after creation)
  before trusting this path again.

## Buffer-connected path (per platform, per package)

1. Applies only after a specific package/platform has reached `approved`
   with a date/time (i.e. `scheduled`) via explicit human instruction —
   Buffer is a delivery mechanism for a decision already made, never a
   new approval path of its own. **Exception**: Instagram may be pushed
   at `review-ready` as a real Buffer draft per the limitation note
   above, since that path is genuinely inert until the human acts.
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
