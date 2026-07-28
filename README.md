# BountyBot feed duplicate-card reproduction

The authenticated BountyBot feed duplicates every current bounty card when
**See bounties I've already seen** is clicked once.

## Evidence

- [12-second reproduction video](./bountybot-feed-duplicate.mp4)
- [Before the click](./before.png)
- [After one click](./after.png)
- [Full report](./report.md)

The captured DOM changed from one to two instances of both
`/add-more-linkedin-followers` and
`/notice-a-bug-on-bountybot-let-us-know`. The full-page height increased from
2,100 px to 3,104 px.

The reproduction, evidence assembly, and write-up were prepared with Codex under
the account holder's supervision.
