---
name: contractor-data-access-review
description: Review contractor, freelancer, consultant, or external partner access to sensitive data, systems, documents, or AI tools. Use when granting temporary or third-party access to internal information.
---

# Contractor Data Access Review

## Purpose

Review the access being granted to a contractor, freelancer, or external partner to identify over-broad permissions, missing agreements, and data that should be restricted or redacted.

## Thinking style

Act as a governance helper and privacy reviewer.

Focus on:

- whether access is scoped to the minimum needed for the task
- whether the right agreements and terms are in place before access is granted
- what happens when the contract ends — is access removed promptly

## Discovery questions

Ask:

1. What is the contractor being engaged to do?
2. What systems, data, or documents do they actually need to do that work?
3. Is there a signed NDA, contract, or data processing agreement in place?
4. Will they be working with personal data about customers, employees, or others?
5. How will access be removed when the engagement ends?

## Workflow

1. Identify what the contractor needs access to for their specific task.
2. Check what access is currently planned or in place.
3. Flag access that is wider than the task requires.
4. Check what agreements are in place.
5. Identify how offboarding will work.

## Checklist

**Access scope:**

- [ ] Is access limited to only what is needed for the specific task?
- [ ] Does the contractor need access to personal data, or can anonymised or test data be used?
- [ ] Does the contractor have access to systems beyond the scope of the engagement?
- [ ] Does the contractor have write or delete permissions when read-only would be sufficient?

**Data involved:**

- [ ] Does the work involve personal data about customers, employees, or others?
- [ ] Does the contractor have access to financial, legal, health, or confidential business data?
- [ ] Could the contractor export or copy data outside the organisation’s systems?

**Agreements and terms:**

- [ ] Is there a signed NDA or confidentiality agreement?
- [ ] Is there a data processing agreement (DPA) if personal data is involved?
- [ ] Does the contract specify what data the contractor can and cannot access or copy?
- [ ] Does the contract specify how data must be handled and returned or deleted at the end?

**AI tools:**

- [ ] Could the contractor use personal AI tools (ChatGPT, Claude) with internal data?
- [ ] Has the organisation’s AI use policy been shared with the contractor?

**Offboarding:**

- [ ] Is there a plan to remove access when the engagement ends?
- [ ] Are accounts time-limited or reviewed on engagement end?
- [ ] Are there shared credentials, API keys, or passwords that will need to be rotated?

## Output format

Return:

- Risk level: low, medium, or high
- Access gaps or over-provisioning identified
- Missing agreements or terms
- AI use risks
- Offboarding gaps
- Recommended changes
- Open questions

## Anti-patterns

Avoid:

- assuming a signed contract covers data access without checking the specific terms
- treating all contractors as trusted employees with equivalent access
- overlooking AI tool use — contractors often use personal AI services with client data
- assuming offboarding will happen automatically without a specific plan
- recommending agreements in principle without checking what is actually signed

## Disclaimer

This is a practical review tool, not legal advice, security certification, or compliance certification.
