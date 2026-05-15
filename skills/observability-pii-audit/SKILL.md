---
name: observability-pii-audit
description: Review observability tools for personal, sensitive, or confidential data exposure in logs, traces, metrics, session replay, errors, prompts, and monitoring platforms. Use when auditing Datadog, Sentry, CloudWatch, New Relic, or similar tools.
---

# Observability PII Audit

## Purpose

Review observability and monitoring tooling to identify where personal data, sensitive content, AI prompts, credentials, or confidential information is being collected and stored by platforms such as Datadog, Sentry, CloudWatch, or New Relic.

## Thinking style

Act as a defensive developer.

Focus on:

- what is flowing into monitoring tools that should not be there
- what third-party monitoring vendors now hold as a result
- whether the organisation has visibility and control over what is collected

## Discovery questions

Ask:

1. Which observability platforms are in use — Datadog, Sentry, New Relic, CloudWatch, Grafana, or others?
2. Are full request or response bodies captured in traces or logs?
3. Are AI prompts, inputs, or outputs being captured in traces or spans?
4. Are session replay tools in use (e.g. FullStory, LogRocket, Datadog RUM) — what do they capture?
5. Who has access to the observability platform, and are access controls in place?

## Workflow

1. List the observability tools in use.
2. For each tool, check what data is captured (logs, traces, metrics, session replay, error reports).
3. Identify personal data, sensitive content, credentials, or AI content in any captured data.
4. Check access controls and retention settings within each tool.
5. Recommend redaction, filtering, or configuration changes.

## Checklist

**Logs:**

- [ ] Are full request or response bodies written to logs?
- [ ] Are user emails, names, or IDs logged?
- [ ] Are API keys, tokens, passwords, or credentials logged?
- [ ] Are AI prompts or AI responses logged?
- [ ] Are health, financial, or other sensitive data fields logged?

**Distributed traces:**

- [ ] Are request payloads captured in trace spans?
- [ ] Are user identifiers or session tokens captured in spans?
- [ ] Are AI prompt or response contents captured in spans?

**Error reporting (e.g. Sentry):**

- [ ] Are error stack traces capturing personal data from request context?
- [ ] Are user email addresses automatically attached to error events?
- [ ] Are breadcrumbs or state objects capturing personal data?

**Session replay:**

- [ ] Is session replay enabled — does it capture form inputs, including password fields?
- [ ] Are personal data fields masked or excluded?
- [ ] Do users know session replay is running?

**Access and retention:**

- [ ] Who has access to the observability platform?
- [ ] Is access limited to engineers who need it?
- [ ] What is the retention period for logs and traces?
- [ ] Does the vendor use observability data for their own purposes?

## Output format

Return:

- Risk level: low, medium, or high
- Personal or sensitive data found in each observability tool
- Credentials or tokens found
- Session replay risks
- Recommended redaction, masking, or configuration changes
- Access and retention recommendations
- Open questions

## Anti-patterns

Avoid:

- treating observability data as internal-only when it is stored in third-party vendor infrastructure
- assuming default settings exclude personal data — most do not
- ignoring session replay as a data capture risk
- recommending generic “review your logging” advice without specific fields or tools
- missing AI prompt and response content in traces — this is an increasingly common PII vector

## Disclaimer

This is a practical review tool, not legal advice, security certification, or compliance certification.
