---
name: api-privacy-review
description: Review APIs for privacy and data exposure risks including excessive fields, weak access boundaries, unsafe identifiers, over-broad responses, logging, retention, and third-party data sharing. Use when designing or auditing API endpoints.
---

# API Privacy Review

## Purpose

Review an API design or existing endpoints for unnecessary data exposure, weak access controls, and privacy risks.

## Thinking style

Act as a defensive developer.

Focus on:

- what data each endpoint returns and whether the caller actually needs all of it
- whether access controls verify the caller’s right to see each specific resource
- what ends up in logs, error messages, and third-party integrations as a side effect of API calls

## Discovery questions

Ask:

1. Which endpoints are being reviewed — are they internal, external, or both?
2. What authentication and authorisation model is in use?
3. Do any endpoints return bulk data or lists of resources?
4. What is logged when an API call is made — are request bodies or response bodies written to logs?
5. Are there any third-party services or webhooks that receive data from these endpoints?

## Workflow

1. List the endpoints being reviewed and what data they return.
2. Check whether responses include more data than the caller needs.
3. Check access controls: who can call each endpoint and with what permissions.
4. Review logging: what data is written to logs.
5. Check third-party integrations and webhooks.
6. Identify retention and deletion gaps.

## Checklist

**Response fields:**

- [ ] Does the response include fields the caller does not need?
- [ ] Are sensitive fields (email, phone, address, health data) returned in any response?
- [ ] Are internal fields (database IDs, system flags, admin notes) exposed to external callers?
- [ ] Are bulk or list endpoints returning more records than necessary?

**Identifiers:**

- [ ] Are sequential or predictable IDs used (e.g. `/users/1234`) that could allow enumeration?
- [ ] Could IDs be used to guess or access other records?

**Access control:**

- [ ] Does each endpoint check that the caller is authorised to access the specific resource?
- [ ] Can a user access another user's data by changing an ID in the request?
- [ ] Are admin or internal endpoints protected from external callers?
- [ ] Are search or filter endpoints limited in how much data they can return?

**Error messages:**

- [ ] Do error messages reveal internal system details, stack traces, or data?

**Logging:**

- [ ] Are full request bodies (which may include personal data) written to logs?
- [ ] Are authentication tokens, passwords, or credentials written to logs?
- [ ] Are AI prompts or responses logged, and if so where and for how long?

**Webhooks and third-party integrations:**

- [ ] Do outbound webhooks send more data than the recipient needs?
- [ ] Are third-party analytics or error monitoring tools receiving personal data?

**Retention and deletion:**

- [ ] Is personal data retained longer than necessary?
- [ ] Is there a way to delete or anonymise data on request?
- [ ] Is test or sandbox data real production data?

## Output format

Return:

- Risk level per endpoint or overall: low, medium, or high
- Key privacy risks found
- Recommended changes
- Safer design alternatives where applicable
- Open questions

## Anti-patterns

Avoid:

- focusing only on obviously sensitive fields and missing derived or inferred data
- treating authentication as equivalent to authorisation — a logged-in user can still access other users’ data
- ignoring error messages as a data exposure vector
- assuming internal APIs do not need access controls
- reviewing only the documented endpoints and missing undocumented or legacy ones

## Disclaimer

This is a practical review tool, not legal advice, security certification, or compliance certification.
