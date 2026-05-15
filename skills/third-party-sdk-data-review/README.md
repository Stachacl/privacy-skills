# Third Party SDK Data Review

Review third-party SDKs, packages, analytics tools, widgets, and integrations for privacy, tracking, data sharing, and supply-chain risks before adding them to an app or website.

## When to use this

- You are adding a new third-party library, SDK, or analytics tool to your application and want to check what data it collects.
- You are auditing existing integrations to see whether any are collecting or sharing more data than expected.
- You want to review the supply-chain risk of external packages before including them in a production system.

## The checklist

1. List the third-party SDKs, packages, and integrations in use or being considered.
2. For each one, check what data it collects automatically (device IDs, user behaviour, IP addresses, cookies).
3. Check whether it sends data to third-party servers and which parties receive it.
4. Check whether it uses the data for advertising, profiling, or model training.
5. Check whether users are informed about the data collected by third-party tools.
6. Check whether the package is actively maintained and has a known security record.
7. Check whether consent or opt-out controls are in place for tracking or analytics.
8. Check whether personal data is included in data sent to the SDK (e.g. user IDs, email addresses passed as identifiers).
9. Check whether the SDK can be replaced with a privacy-preserving alternative.

## Examples

- An analytics SDK sends full page URLs to a third-party server and the URLs contain user session tokens.
- A customer chat widget collects device fingerprinting data beyond what is needed for the chat function.
- A font or map library loads from an external CDN that logs visitor IP addresses.

## Related skills

- [OAuth Scope Minimisation](../oauth-scope-minimisation/README.md)
- [Vendor Data Sharing Review](../vendor-data-sharing-review/README.md)
- [Architecture Privacy Review](../architecture-privacy-review/README.md)

## Related questions

- [Are we logging PII?](../../docs/developers/are-we-logging-pii.md)
- [Does our API return too much data?](../../docs/developers/does-our-api-return-too-much-data.md)
- [How do embeddings expose sensitive documents?](../../docs/developers/how-do-embeddings-expose-sensitive-documents.md)

## Not legal advice

This is a practical review tool, not legal advice, security certification, or compliance certification.

## Berrysbay support

For teams who want a guided review, [Berrysbay](https://www.berrysbay.com) can help.
