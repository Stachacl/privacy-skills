# OAuth Scope Minimisation

Review OAuth permissions and app scopes for excessive access, unnecessary permissions, and safer alternatives when integrating with Google, Microsoft, Slack, GitHub, or other OAuth providers.

## When to use this

- You are adding an OAuth integration and want to check whether the requested scopes are appropriate.
- You are auditing existing app integrations to see whether any have more access than they need.
- You are reviewing third-party apps connected to your Google Workspace, Microsoft 365, or Slack account.

## The checklist

1. List the OAuth scopes being requested by the integration.
2. For each scope, confirm it is needed for the actual functionality of the integration.
3. Check whether a narrower or read-only version of the scope could be used instead.
4. Check whether any scopes grant access to data outside the app's stated purpose (e.g. access to contacts, calendar, or email when not needed).
5. Check whether the app can access data on behalf of all users or only the authorising user.
6. Check whether access tokens are stored securely and rotated appropriately.
7. Review what the third party does with the data it accesses.
8. Check whether the integration can be revoked easily if no longer needed.

## Examples

- A task management integration requests read and write access to all Google Drive files when it only needs to create files in a specific folder.
- A Slack bot requests access to read all messages in all channels when it only needs to post to one channel.
- A GitHub integration requests write access to all repositories when it only needs to read a single repository for CI status.

## Related skills

- [Third Party SDK Data Review](../third-party-sdk-data-review/README.md)
- [Vendor Data Sharing Review](../vendor-data-sharing-review/README.md)
- [Architecture Privacy Review](../architecture-privacy-review/README.md)

## Related questions

- [Does our API return too much data?](../../docs/developers/does-our-api-return-too-much-data.md)
- [Are we logging PII?](../../docs/developers/are-we-logging-pii.md)
- [How to manage shadow AI](../../docs/teams/how-to-manage-shadow-ai.md)

## Not legal advice

This is a practical review tool, not legal advice, security certification, or compliance certification.

## Berrysbay support

For teams who want a guided review, [Berrysbay](https://www.berrysbay.com) can help.
