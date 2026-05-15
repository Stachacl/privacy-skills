# Data Minimisation Review

Review what personal data is being collected and retained to identify what can be reduced, removed, anonymised, or replaced with a less specific version.

## When to use this

- You are auditing a form, database, or data collection process and want to reduce unnecessary collection.
- You are preparing for a privacy review and need to justify every field you collect.
- You want to simplify your data model and reduce the risk of holding data you do not need.

## The checklist

1. List every personal data field or dataset being collected.
2. For each field, ask: why is this needed, and what happens if it is not collected?
3. Check whether a less specific version could be used (e.g. age range instead of date of birth).
4. Check whether any fields are collected but rarely or never actually used.
5. Check whether free-text fields are encouraging people to share more than necessary.
6. Check whether data is stored in multiple places unnecessarily.
7. Check whether old records are retained beyond their useful life.
8. Check whether full personal data is shared with third parties or analytics tools when only a subset is needed.
9. Check whether there is a retention policy and whether it is enforced.

## Examples

- A sign-up form collects full date of birth, phone number, and postal address, but the service only ever uses an email address and first name.
- A CRM stores detailed freehand notes about customer conversations that include sensitive personal disclosures far beyond what the support team needs.
- Analytics tracking sends full URLs to a third-party tool, and the URLs contain user IDs and search queries.

## Related skills

- [Form Privacy Check](../form-privacy-check/README.md)
- [Minimum Data Needed](../minimum-data-needed/README.md)
- [Data Retention Policy Builder](../data-retention-policy-builder/README.md)

## Related questions

- [Does our API return too much data?](../../docs/developers/does-our-api-return-too-much-data.md)
- [Are we logging PII?](../../docs/developers/are-we-logging-pii.md)
- [Can I upload this to an AI tool?](../../docs/everyday/can-i-upload-this-to-ai.md)

## Not legal advice

This is a practical review tool, not legal advice, compliance certification, or a formal privacy impact assessment.

## Berrysbay support

For teams who want a guided review, [Berrysbay](https://www.berrysbay.com) can help.
