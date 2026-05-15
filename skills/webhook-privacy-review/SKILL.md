---
name: webhook-privacy-review
description: Review webhooks for privacy and data exposure risks, including payload design, secrets, retries, logs, third-party endpoints, excessive fields, and retention. Use when designing or auditing webhook integrations.
---

# Webhook Privacy Review

## Purpose

Review webhook design and configuration to identify where personal data is over-shared in payloads, where secrets or verification are weak, and where retry or logging behaviour creates data exposure risks.

## Thinking style

Act as a defensive developer.

Focus on:

- whether webhook payloads contain more data than the receiver needs
- whether payload delivery and retry create unexpected data persistence
- whether the receiving endpoint is trusted and secured

## Discovery questions

Ask:

1. What event or trigger sends the webhook, and what data is included in the payload?
2. Who or what receives the webhook — an internal service, a third-party platform, or an external partner?
3. Is the receiving endpoint validated as belonging to the intended recipient?
4. What happens when a webhook fails — is the payload retried, queued, or logged?
5. Is the payload stored anywhere after delivery?

## Workflow

1. Identify the webhook trigger and the data included in the payload.
2. Check whether the payload contains more data than the receiver needs.
3. Check whether the receiving endpoint is authenticated and verified.
4. Check retry, queuing, and logging behaviour.
5. Check third-party platforms: where does the payload go and what do they do with it?

## Checklist

**Payload design:**

- [ ] Does the payload include personal data (names, emails, addresses, health, financial)?
- [ ] Does the payload include more fields than the receiver needs?
- [ ] Could the payload be replaced with a minimal notification plus a lookup (thin payload pattern)?
- [ ] Does the payload include internal IDs or system fields not needed externally?

**Authentication and verification:**

- [ ] Is the receiving endpoint authenticated (e.g. HMAC signature, shared secret)?
- [ ] Is the signature verified before processing the payload?
- [ ] Is the endpoint HTTPS?
- [ ] Is the receiving domain validated — could the endpoint be hijacked by a DNS change?

**Retry and queuing:**

- [ ] Are failed webhook payloads stored in a retry queue?
- [ ] How long are queued payloads retained?
- [ ] Does the retry queue include personal data in plaintext?
- [ ] Is the queue access-controlled?

**Logging:**

- [ ] Are full webhook payloads written to logs?
- [ ] Are logs redacted before writing personal data from payloads?
- [ ] Who has access to webhook logs?

**Third-party platforms:**

- [ ] If the webhook goes to a third-party service (e.g. Zapier, Make, Slack), what do they do with the data?
- [ ] Does the third-party platform retain payload content?
- [ ] Is there a DPA with the third-party platform?

## Output format

Return:

- Risk level: low, medium, or high
- Payload data exposure issues
- Authentication or verification gaps
- Retry and logging risks
- Third-party platform risks
- Recommended changes
- Open questions

## Anti-patterns

Avoid:

- sending full object payloads when a thin notification with an ID would be sufficient
- assuming HTTPS is sufficient verification — the endpoint still needs to verify the sender
- ignoring retry queues as a data persistence vector
- treating Zapier or Make as internal systems — they are third-party data processors
- recommending “log less” without specifying which fields to redact

## Disclaimer

This is a practical review tool, not legal advice, security certification, or compliance certification.
