# Architecture Privacy Review

Review a system or software architecture for privacy risks, including data flows, third-party dependencies, storage, access control, and logging.

## When to use this

- You are assessing a new architecture before building or launching a product.
- You are reviewing an existing system ahead of an audit or significant change.
- You want to map where personal data is handled across your technical stack.

## The checklist

1. Identify the components in the architecture: services, databases, APIs, queues, third-party tools.
2. Map which components handle personal or sensitive data.
3. Trace data flows between components and check whether personal data is passed unnecessarily.
4. Check whether personal data is sent to third-party services or AI providers.
5. Review storage: where is personal data kept, is it encrypted at rest, are backups protected?
6. Check access controls: which services and people can access personal data, are role-based controls in place?
7. Check whether data is encrypted in transit between services.
8. Review logs: do they contain personal data, and are log access controls in place?
9. Check third-party dependencies for data processing agreements.

## Examples

- A microservices system passes a full user object (including health data) between services even when only a user ID is needed.
- An internal admin tool is accessible without authentication from within the corporate network.
- Application logs contain full JSON request bodies, including customer email addresses and phone numbers.

## Related skills

- [Data Flow Mapping](../data-flow-mapping/README.md)
- [Logging Privacy Review](../logging-privacy-review/README.md)
- [Privacy by Design Review](../privacy-by-design-review/README.md)

## Related questions

- [Are we logging PII?](../../docs/developers/are-we-logging-pii.md)
- [Does our API return too much data?](../../docs/developers/does-our-api-return-too-much-data.md)
- [How do embeddings expose sensitive documents?](../../docs/developers/how-do-embeddings-expose-sensitive-documents.md)

## Not legal advice

This is a practical review tool, not legal advice, security certification, or compliance certification.

## Berrysbay support

For teams who want a guided review, [Berrysbay](https://www.berrysbay.com) can help.
