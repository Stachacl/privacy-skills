---
name: privacy-by-design-review
description: Review a project, feature, product, or workflow against privacy-by-design principles, including minimisation, purpose limitation, access control, transparency, retention, secure defaults, and safer architecture. Use when planning a new product or feature, or before launch.
---

# Privacy by Design Review

## Purpose

Review a project, feature, or workflow early to identify privacy risks and build better defaults before launch.

Privacy by design is about making good choices at the start rather than fixing problems later.

## Thinking style

Act as a privacy reviewer and architecture reviewer.

Focus on:

- identifying where privacy trade-offs are being made and whether they are intentional
- checking defaults — the most privacy-protective option should be the default, not opt-in
- asking questions the team may not have considered, especially around third parties and AI

## Discovery questions

Ask:

1. What is being built or changed, and at what stage — design, build, or pre-launch?
2. Whose personal data is involved, and what type?
3. Are there any third-party services, SDKs, or AI tools involved that will handle personal data?
4. What are the default settings for data sharing and visibility — who can see what by default?
5. Has the team thought about how people can access, correct, or delete their data?

## Workflow

1. Describe the project or feature being reviewed.
2. Identify what personal or sensitive data is involved.
3. Work through the checklist below.
4. Identify gaps and recommend changes.
5. Flag anything that needs specialist review.

## Checklist

**Purpose:**

- [ ] Is there a clear reason for collecting this data?
- [ ] Is the purpose specific and limited?
- [ ] Will the data only be used for the stated purpose?

**Data minimisation:**

- [ ] Is only the minimum data necessary being collected?
- [ ] Are there fields that could be removed or made optional?

**Collection:**

- [ ] Is data collected directly from the person or from a third party?
- [ ] Is the collection method transparent?

**Consent and notice:**

- [ ] Do people know their data is being collected?
- [ ] Is there a way for people to opt out or request deletion?

**Access control:**

- [ ] Who can access this data?
- [ ] Is access limited to people who need it?
- [ ] Are there role-based permissions in place?

**Default settings:**

- [ ] Are the defaults the most privacy-protective option?
- [ ] Must users opt in to sharing, or opt out?

**Retention:**

- [ ] How long is data kept?
- [ ] Is there an automatic deletion or anonymisation process?

**Deletion:**

- [ ] Can data be deleted on request?
- [ ] Is deletion propagated to backups, caches, and third-party systems?

**Vendor and third-party sharing:**

- [ ] What data is shared with external services (analytics, AI, cloud providers)?
- [ ] Are data processing agreements in place?

**AI use:**

- [ ] Is AI involved in processing or making decisions about personal data?
- [ ] Are prompts, inputs, or outputs stored or used for training?

**Logging:**

- [ ] Do application logs contain personal data?
- [ ] Are logs protected and access-controlled?

**Security basics:**

- [ ] Is data encrypted in transit and at rest?
- [ ] Are authentication and authorisation controls in place?

**Safer alternatives:**

- [ ] Is there a way to achieve the same outcome with less data?
- [ ] Could aggregated or anonymised data be used instead?

## Output format

Return:

- Overall risk level: low, medium, or high
- Key privacy risks found
- Recommended changes by priority
- Areas requiring specialist legal or security review
- Safer design alternatives where applicable
- Open questions

## Anti-patterns

Avoid:

- treating privacy by design as a checklist to complete rather than a design influence
- reviewing only the main feature and missing the logging, analytics, and error reporting that surround it
- accepting “we’ll add privacy controls later” as a plan
- assuming GDPR compliance means good privacy design — they are not the same
- producing a long risk list without recommending specific design changes

## Disclaimer

This is a practical review tool, not legal advice, compliance certification, or a formal privacy impact assessment.
