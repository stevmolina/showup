# Publishing operations

Read this reference for Typefully drafts, schedules, publishing, or social-account actions.

Read [platform fit](platforms.md) when adapting approved copy for a destination.

Typefully is the sole delivery adapter for this version. Keep publisher-specific IDs and state out of the skill logic except where needed to call Typefully. Notion remains the canonical content record.

## Typefully

1. Discover the connected social sets and identify the intended account by stable ID.
2. Inspect the queue and timezone when timing matters.
3. Create platform-specific content. Save privately as a draft unless Steven authorized another state.
4. Verify the returned draft ID, status, and private URL.
5. Fetch the draft or draft list when later state matters.
6. Write the verified Typefully item ID, review URL, platform, status, and relevant timestamp back to the matching Notion record.

Discover the live tool schema before each write. Tool fields and connected platforms may change. A social set does not imply that every platform is connected.

## Authorization

A request to draft permits drafting in chat. A request to save or queue a private draft permits that private write. Publishing, scheduling, replying, liking, reposting, deleting, following, and sending DMs require explicit authorization for the exact account, content, and action.

After a private write, report the platform, account, status, and review URL. After scheduling or publishing, verify the final state and return its URL.
