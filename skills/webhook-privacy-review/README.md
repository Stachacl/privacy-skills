# Webhook Privacy Review

Review webhooks for privacy and data exposure risks, including payload design, secrets, retries, logs, third-party endpoints, excessive fields, and retention.

## When to use this

- You are designing or auditing webhook integrations and want to check what data they expose.
- You want to review whether outbound webhooks send more data than the recipient needs.
- You are checking whether webhook secrets, retries, and logs are handled safely.

## The checklist

1. List the webhooks being sent and received and what data each payload contains.
2. Check whether payloads include more fields than the recipient needs.
3. Check whether payloads include personal data (names, emails, IDs, addresses).
4. Check whether webhook endpoints are authenticated using a shared secret or signature verification.
5. Check whether secrets are stored securely and rotated appropriately.
6. Check whether failed webhook deliveries are retried, and whether retried payloads containing personal data are logged.
7. Check whether webhook payloads are written to logs and whether those logs are appropriately protected.
8. Check whether the receiving endpoint is a third-party service and what that party does with the data.
9. Check whether there is a process to rotate webhook secrets if they are compromised.
10. Check how long webhook logs and failed delivery records are retained.

## Examples

- A payment webhook sends the full customer record to a third-party logistics system when only an order ID and fulfilment status are needed.
- Webhook payloads containing customer emails and order details are written to a debug log retained for 90 days with no access controls.
- A webhook secret is hardcoded in a public repository, allowing anyone to send arbitrary events to the endpoint.

## Related skills

- [API Privacy Review](../api-privacy-review/README.md)
- [Logging Privacy Review](../logging-privacy-review/README.md)
- [Third Party SDK Data Review](../third-party-sdk-data-review/README.md)

## Related questions

- [Does our API return too much data?](../../docs/developers/does-our-api-return-too-much-data.md)
- [Are we logging PII?](../../docs/developers/are-we-logging-pii.md)
- [How do embeddings expose sensitive documents?](../../docs/developers/how-do-embeddings-expose-sensitive-documents.md)

## Not legal advice

This is a practical review tool, not legal advice, security certification, or compliance certification.

## Berrysbay Labs support

For teams who want a guided review, [Berrysbay Labs](https://www.berrysbay.com) can help.
