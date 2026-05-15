# API Privacy Review

Review API endpoints for unnecessary data exposure, weak access controls, unsafe identifiers, and privacy risks in responses, logs, and third-party integrations.

## When to use this

- You are designing new API endpoints and want to check what data they will return.
- You are auditing existing endpoints before a launch or security review.
- You have noticed that API responses include more fields than callers actually need.

## The checklist

1. List the endpoints being reviewed and what data they return.
2. Check whether responses include fields the caller does not need.
3. Check whether sensitive fields (email, phone, health data, financial data) appear in any response.
4. Check whether internal fields (database IDs, system flags, admin notes) are exposed to external callers.
5. Check whether sequential or predictable IDs are used (e.g. `/users/1234`) that could allow enumeration.
6. Confirm that each endpoint checks the caller is authorised to access the specific resource, not just authenticated.
7. Check whether a user can access another user's data by changing an ID in the request.
8. Check whether full request bodies containing personal data are written to logs.
9. Check whether tokens, passwords, or credentials are ever logged.
10. Check whether outbound webhooks or third-party analytics tools receive more data than necessary.

## Examples

- A user profile endpoint returns internal admin flags, account balance, and full address even when the caller only needs a display name.
- A support API uses sequential numeric IDs, allowing a caller to iterate through customer records.
- Error responses include full stack traces revealing database table names and internal field names.

## Related skills

- [Logging Privacy Review](../logging-privacy-review/README.md)
- [Data Minimisation Review](../data-minimisation-review/README.md)
- [Architecture Privacy Review](../architecture-privacy-review/README.md)

## Related questions

- [Does our API return too much data?](../../docs/developers/does-our-api-return-too-much-data.md)
- [Are we logging PII?](../../docs/developers/are-we-logging-pii.md)
- [How do embeddings expose sensitive documents?](../../docs/developers/how-do-embeddings-expose-sensitive-documents.md)

## Not legal advice

This is a practical review tool, not legal advice, security certification, or compliance certification.

## About

Created by [Berrysbay Labs](https://www.berrysbay.com) as part of an open-source effort to make privacy thinking more practical for teams building with AI, cloud tools, and sensitive data.

Berrysbay Labs focuses on AI data exposure, local-first and on-prem AI systems, and tools that help reduce sensitive information before it leaves a device or organisation.
