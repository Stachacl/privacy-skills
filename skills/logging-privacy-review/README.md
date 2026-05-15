# Logging Privacy Review

Review what an application or system writes to logs to check whether personal data, credentials, or AI content is being stored unnecessarily.

## When to use this

- You are auditing your logging setup before a privacy review or security assessment.
- You are setting up a new logging pipeline and want to build good defaults from the start.
- You have noticed that logs may contain personal data or sensitive content and want to assess the risk.

## The checklist

1. Identify the logging tools and log destinations in use (local, cloud, third-party service).
2. List what events and data are logged.
3. Check whether full request or response bodies are logged (these may contain personal data).
4. Check whether user email addresses, names, or IDs are written to logs.
5. Check whether health, financial, or other sensitive fields appear in logs.
6. Check whether AI prompts or AI responses are logged, and where and for how long.
7. Check whether authentication tokens, passwords, or API keys are ever logged.
8. Check whether error messages reveal personal data or internal system details.
9. Check who has access to the logs.
10. Check whether third-party tools (Datadog, Sentry, Splunk, etc.) are receiving personal data.
11. Check log retention: how long are logs kept, and is there an automatic rotation or deletion policy?
12. Check whether log scrubbing or redaction filters are in place.

## Examples

- An API logs the full JSON request body for every request, including user addresses and payment tokens.
- A third-party error tracking service captures exception messages that include customer email addresses from session context.
- AI prompt content is written to a debug log that is accessible to all engineers without restriction.

## Related skills

- [Observability PII Audit](../observability-pii-audit/README.md)
- [API Privacy Review](../api-privacy-review/README.md)
- [Architecture Privacy Review](../architecture-privacy-review/README.md)

## Related questions

- [Are we logging PII?](../../docs/developers/are-we-logging-pii.md)
- [Does our API return too much data?](../../docs/developers/does-our-api-return-too-much-data.md)
- [How do embeddings expose sensitive documents?](../../docs/developers/how-do-embeddings-expose-sensitive-documents.md)

## Not legal advice

This is a practical review tool, not legal advice, security certification, or compliance certification.

## Berrysbay support

For teams who want a guided review, [Berrysbay](https://www.berrysbay.com) can help.
