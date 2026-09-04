---
name: showup-publish
description: Save, queue, schedule, publish, or manage Steven's approved personal social content through Typefully and connected accounts. Use when he asks to put a draft in Typefully or perform a specific social-account action.
---

# Show Up publish

Move approved copy into the requested private or public state.

Typefully is the canonical delivery adapter. Notion owns content history and approval; Typefully owns drafts, queues, schedules, and publication state.

Read [publishing operations](../../references/publishing.md). Read [Steven's social voice](../../references/voice.md) when adapting copy before the write.

## Workflow

1. Resolve the exact Typefully social set, account, and platform from live connected-account data.
2. Preserve the approved copy. Make platform changes only when Steven requested adaptation or the destination requires one.
3. Apply the authorization boundary in the publishing reference.
4. Perform the requested write once. If the service rejects it, inspect the error and use a documented fallback only when the requested outcome permits that destination.
5. Fetch or inspect the resulting item to verify account, content, status, and timing.
6. When the post belongs to a Notion content record, fetch the live Content Inbox schema and record the verified Typefully item ID, review URL, platform, final approved copy, status, and scheduled or published time.

## Done

The operation is complete when the requested state is verified and Steven receives the account, platform, status, and review or public URL. Report failures plainly and never claim that a draft, schedule, or post exists without an ID or fetched state.
