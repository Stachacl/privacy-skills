# Does our API return too much data?

## Short answer

Probably. Most APIs accumulate extra fields over time, and it is common to return the full object from a database query rather than only what the caller needs. Over-broad responses expose data unnecessarily and make it harder to control what information reaches different callers.

## What to check

1. List the endpoints being reviewed and what data they currently return.
2. For each endpoint, identify which fields the calling client actually uses.
3. Check whether responses include fields the caller does not need — especially sensitive fields like email, phone, address, health data, or financial data.
4. Check whether internal fields (database IDs, system flags, admin notes, internal metadata) are returned to external callers.
5. Check whether bulk or list endpoints return more records than necessary — are there appropriate pagination and filtering limits?
6. Check whether sequential or predictable IDs are used (e.g. `/users/1234`) that could allow a caller to iterate through records.
7. Check whether each endpoint verifies that the caller is authorised to access the specific resource, not just authenticated.
8. Check whether a user can access another user's data by changing an ID in the request (insecure direct object reference).
9. Check whether search or filter endpoints have appropriate limits on how much data they can return.
10. Check whether error responses include internal details, stack traces, or database field names.

**Common patterns that lead to over-broad APIs:**

- Returning the full database row rather than a projection of needed fields
- Reusing a large "full user" response object across multiple endpoints with different permission levels
- Admin endpoints accessible to non-admin callers without proper access control checks
- Error messages that include internal table names, query details, or stack traces

## Use this skill

[API Privacy Review](../../skills/api-privacy-review/README.md) — full checklist for reviewing API endpoints for data exposure and access control risks.

[Data Minimisation Review](../../skills/data-minimisation-review/README.md) — review what data is collected and returned across your system.

## Related questions

- [Are we logging PII?](are-we-logging-pii.md)
- [How do embeddings expose sensitive documents?](how-do-embeddings-expose-sensitive-documents.md)
- [Can I upload this to an AI tool?](../everyday/can-i-upload-this-to-ai.md)
- [How to build an AI use policy](../teams/how-to-build-an-ai-use-policy.md)

## Not legal advice

This is a practical review tool, not legal advice, security certification, or compliance certification.
