---
name: logging-privacy-review
description: Review application, server, or AI system logs for personal data, sensitive information, credentials, or AI prompt content that should not be stored. Use when auditing logging practices or setting up a new logging pipeline.
---

# Logging Privacy Review

## Purpose

Review what an application or system is writing to logs to check whether personal data, credentials, or AI content is being stored unnecessarily.

## Thinking style

Act as a defensive developer.

Focus on:

- what is actually flowing into logs, not just what is supposed to be logged
- third-party logging services as a data sharing destination
- credentials and tokens in logs as a separate high-severity category from personal data

## Discovery questions

Ask:

1. What logging tools and destinations are in use — local files, cloud logging, Datadog, Sentry?
2. Are request or response bodies logged at any log level?
3. Are AI prompts or responses captured in logs or traces?
4. Who has access to the logs, including any third-party platforms?
5. Is there an existing redaction or scrubbing policy?

## Workflow

1. Identify the logging tools and log destinations in use.
2. List what events and data are logged.
3. Check for personal data, sensitive content, or credentials in log fields.
4. Review log retention, access control, and deletion.
5. Recommend redaction, filtering, or log level changes.

## Checklist

**What is being logged:**

- [ ] Are full request or response bodies logged (which may include personal data)?
- [ ] Are user email addresses, names, or IDs written to logs?
- [ ] Are health, financial, or other sensitive fields written to logs?
- [ ] Are AI prompts or AI responses written to logs?
- [ ] Are authentication tokens, passwords, or API keys logged?
- [ ] Are error messages revealing personal data or internal system details?

**Log destination and access:**

- [ ] Where are logs stored (local, cloud, third-party logging service)?
- [ ] Who has access to logs?
- [ ] Are third-party tools (e.g. Datadog, Sentry, Splunk) receiving personal data?

**Retention and deletion:**

- [ ] How long are logs retained?
- [ ] Is there an automatic deletion or rotation policy?
- [ ] Can specific log entries be deleted on request?

**Redaction and filtering:**

- [ ] Are there log scrubbing or redaction filters in place?
- [ ] Are sensitive fields masked or replaced before logging?

## Output format

Return:

- Risk level: low, medium, or high
- Personal or sensitive data found in logs
- Credentials or tokens found in logs
- Recommended redaction or filtering changes
- Retention and access recommendations
- Open questions

## Anti-patterns

Avoid:

- reviewing only production logs and missing staging, debug, or error reporting tools
- treating credentials in logs as a lower priority than personal data — they are often higher
- recommending “don’t log sensitive fields” without identifying which specific fields to redact
- assuming structured logging is safer than unstructured — structured logs still capture what is passed to them
- ignoring retention — a log that captures minimal data but is retained indefinitely is still a risk

## Disclaimer

This is a practical review tool, not legal advice, security certification, or compliance certification.
