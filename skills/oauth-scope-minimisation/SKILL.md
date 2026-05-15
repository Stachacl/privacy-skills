---
name: oauth-scope-minimisation
description: Review OAuth permissions and app scopes for excessive access, unnecessary permissions, sensitive data exposure, and safer alternatives. Use when integrating with Google, Microsoft, Slack, GitHub, or other OAuth providers.
---

# OAuth Scope Minimisation

## Purpose

Review OAuth permissions and app scopes to identify where an application is requesting broader access than it needs, and recommend the minimum scopes required.

## Thinking style

Act as a defensive developer.

Focus on:

- whether requested scopes are proportionate to the actual use case
- which scopes grant access to personal or sensitive data
- what an attacker could do with a compromised token carrying these scopes

## Discovery questions

Ask:

1. Which OAuth provider is being integrated — Google, Microsoft, Slack, GitHub, or another?
2. What does the integration actually need to do?
3. What scopes are currently requested or planned?
4. Are any scopes read/write when read-only would be sufficient?
5. How long are tokens stored, and can they be revoked?

## Workflow

1. List the scopes being requested.
2. For each scope, identify what data or access it grants.
3. Check whether the scope is necessary for the integration’s actual function.
4. Identify scopes that grant access to sensitive data unnecessarily.
5. Recommend the minimum viable scope set.

## Checklist

**Scope necessity:**

- [ ] Is each scope actually used by the integration?
- [ ] Are any scopes included “just in case” for future use?
- [ ] Is write access requested when read-only is sufficient?
- [ ] Are broad scopes used when narrower alternatives exist?

**Sensitive data access:**

- [ ] Does any scope grant access to email content?
- [ ] Does any scope grant access to calendar details or meeting content?
- [ ] Does any scope grant access to contacts or directory information?
- [ ] Does any scope grant access to files or documents?
- [ ] Does any scope grant access to admin or management APIs?

**Token handling:**

- [ ] How are tokens stored — in a database, secrets manager, or environment variable?
- [ ] Is token storage encrypted?
- [ ] What is the token expiry period?
- [ ] Is there a process to revoke tokens if the integration is retired or compromised?
- [ ] Are refresh tokens stored, and are they protected?

**User consent:**

- [ ] Are users shown the full scope list at consent time?
- [ ] Is the requested access proportionate to what users would expect?
- [ ] Is there an incremental consent flow (request scopes only when needed)?

## Output format

Return:

- Risk level: low, medium, or high
- Scopes that exceed the minimum needed
- Scopes that grant access to sensitive data
- Recommended minimum scope set
- Token storage and revocation recommendations
- Open questions

## Anti-patterns

Avoid:

- requesting broad scopes now “in case we need them later”
- treating OAuth tokens as less sensitive than passwords — they grant equivalent access
- assuming read-only scopes carry no risk — read access to email or calendars is highly sensitive
- ignoring token revocation — tokens persist after an integration is removed unless explicitly revoked
- skipping user consent review because the integration is internal

## Disclaimer

This is a practical review tool, not legal advice, security certification, or compliance certification.
