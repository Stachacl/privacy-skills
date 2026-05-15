# Observability PII Audit

Review observability tools for personal, sensitive, or confidential data exposure in logs, traces, metrics, session replay, errors, and monitoring platforms.

## When to use this

- You are auditing Datadog, Sentry, CloudWatch, New Relic, or a similar monitoring platform for personal data.
- You are setting up a new observability stack and want to avoid capturing PII from the start.
- You want to check whether session replay tools are capturing sensitive form fields or user input.

## The checklist

1. List the observability tools in use: logging, tracing, metrics, error tracking, session replay.
2. Check whether logs contain personal data: names, emails, IDs, addresses, or contact details.
3. Check whether distributed traces carry personal data in span attributes or request metadata.
4. Check whether error reports include personal data from request context, stack frames, or error messages.
5. Check whether session replay tools are capturing sensitive form fields, free-text inputs, or PII.
6. Check whether AI prompts or AI responses are flowing into any observability tool.
7. Check who has access to the observability tools and whether access is appropriately restricted.
8. Check where data is stored and in which region.
9. Check retention settings: how long is data kept in each tool?
10. Check whether scrubbing, masking, or filtering rules are in place for sensitive fields.

## Examples

- Sentry is capturing full request bodies in error events, including customer email addresses and order details.
- A session replay tool is recording keystrokes in a password reset form because the input was not explicitly excluded.
- Distributed traces include a user ID that maps to sensitive health information stored in another service.

## Related skills

- [Logging Privacy Review](../logging-privacy-review/README.md)
- [API Privacy Review](../api-privacy-review/README.md)
- [Architecture Privacy Review](../architecture-privacy-review/README.md)

## Related questions

- [Are we logging PII?](../../docs/developers/are-we-logging-pii.md)
- [Does our API return too much data?](../../docs/developers/does-our-api-return-too-much-data.md)
- [How do embeddings expose sensitive documents?](../../docs/developers/how-do-embeddings-expose-sensitive-documents.md)

## Not legal advice

This is a practical review tool, not legal advice, security certification, or compliance certification.

## About

Created by [Berrysbay Labs](https://www.berrysbay.com) as part of an open-source effort to make privacy thinking more practical for teams building with AI, cloud tools, and sensitive data.

Berrysbay Labs focuses on AI data exposure, local-first and on-prem AI systems, and tools that help reduce sensitive information before it leaves a device or organisation.
