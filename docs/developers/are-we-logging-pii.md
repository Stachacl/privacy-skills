# Are we logging PII?

## Short answer

Probably, unless you have specifically designed your logging to avoid it. Most applications log more than they need to, and personal data ends up in logs because request bodies, error messages, and user context are logged by default. The fix is to audit what is in your logs, add redaction for sensitive fields, and tighten retention.

## What to check

1. List your logging tools and where logs are stored (local, cloud, third-party service like Datadog, Sentry, or Splunk).
2. Check whether full request bodies are logged — these often contain form data, JSON payloads, and personal details.
3. Check whether full response bodies are logged — responses may return personal data that should not be stored in logs.
4. Check whether user identifiers (email addresses, names, user IDs) appear in logs.
5. Check whether health, financial, or other sensitive fields ever appear in log events.
6. Check whether AI prompts or AI responses are written to any log.
7. Check whether authentication tokens, passwords, or API keys appear in logs.
8. Check whether error messages include user data or stack traces revealing internal structure.
9. Check who has access to logs — are they accessible to all engineers, or access-controlled?
10. Check whether third-party observability tools receive personal data in event payloads.
11. Check log retention: how long are logs kept, and is there an automatic rotation or deletion policy?
12. Check whether field-level scrubbing or redaction filters are in place.

**Common places PII appears in logs:**

- HTTP request logs (query parameters, request bodies)
- Exception and error logs (user context, session data)
- AI system logs (prompts, completions, retrieved document chunks)
- Audit logs (who accessed what, with what data)
- Third-party error tracking events

## Use this skill

[Logging Privacy Review](../../skills/logging-privacy-review/README.md) — full audit checklist for application and system logs.

[Observability PII Audit](../../skills/observability-pii-audit/README.md) — specific review for Datadog, Sentry, New Relic, and similar tools.

## Related questions

- [Does our API return too much data?](does-our-api-return-too-much-data.md)
- [How do embeddings expose sensitive documents?](how-do-embeddings-expose-sensitive-documents.md)
- [Can I upload this to an AI tool?](../everyday/can-i-upload-this-to-ai.md)
- [How to build an AI use policy](../teams/how-to-build-an-ai-use-policy.md)

## Not legal advice

This is a practical review tool, not legal advice, security certification, or compliance certification.
