# Feed history control duplicates the current bounty cards

## Summary

On the authenticated `/feed` page, clicking **See bounties I've already seen**
appends a second copy of every bounty card that is already visible. It does not
show a distinct history and leaves the feed with duplicate links, rewards, slot
counts, and descriptions.

## Reproduction

1. Sign in and open `https://bountybot.com/feed`.
2. Scroll to the end of the four-card feed.
3. Click **See bounties I've already seen** once.
4. Observe that the same four cards are appended again.

## Expected

The control should reveal previously viewed bounties that are not already in the
current feed, or show an empty-history state when no distinct records exist.

## Actual

All four current cards are rendered twice. In the captured run:

- `/add-more-linkedin-followers` appeared once before the click and twice after.
- `/notice-a-bug-on-bountybot-let-us-know` appeared once before the click and
  twice after.
- The full-page height increased from 2,100 px to 3,104 px.

## Impact

The feed becomes misleading and repetitive. Users cannot tell whether a card is
new, current, or historical, and repeated clicks can make the page unnecessarily
long.

## Evidence

- `before.png`: one copy of each current card and the history control.
- `after.png`: the same cards duplicated after one click.
- `bountybot-feed-duplicate.mp4`: concise reproduction video.

This is a normal UI/data-deduplication defect, not a security issue.

## Disclosure

The reproduction, evidence assembly, and write-up were prepared with Codex under
the account holder's supervision.
