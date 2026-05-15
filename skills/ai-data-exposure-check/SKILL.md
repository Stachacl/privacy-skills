---
name: ai-data-exposure-check
description: Check whether personal, customer, employee, or confidential business data is being exposed through AI tools, prompts, responses, integrations, or training pipelines. Use when auditing AI use across a team or organisation.
---

# AI Data Exposure Check

## Purpose

Review how AI tools are being used across a team or organisation to identify where personal or sensitive data may be exposed, stored, logged, or shared unintentionally.

## Thinking style

Act as a privacy reviewer.

Focus on:

- actual AI tool use vs what policy says should happen
- shadow AI and unapproved tools staff are using without oversight
- logging, training use, and vendor data handling clauses that are often overlooked

## Project context

This skill is part of the Berrysbay Labs Privacy Skills collection: open-source practical review tools for privacy, AI data exposure, sensitive data workflows, local AI, and practical AI governance.

## Discovery questions

Ask:

1. What AI tools are staff using — list both approved and any unapproved tools you know of?
2. Are staff using consumer or enterprise versions of these tools?
3. What types of data does the organisation handle (customer, employee, health, financial)?
4. Are there existing AI use policies or data restrictions in place?
5. Have there been any recent concerns or incidents involving AI and data exposure?

## Workflow

1. List the AI tools in use (consumer and enterprise).
2. For each tool, identify what data is being shared via prompts, uploads, or integrations.
3. Check whether prompts or responses are logged or used for training.
4. Check whether third-party AI integrations have access to internal data.
5. Identify gaps and recommend safer practices.

## Checklist

**Prompt content:**

- [ ] Are staff pasting customer or personal data into prompts?
- [ ] Are internal documents uploaded to consumer AI tools?
- [ ] Are prompts containing confidential business information?

**Logging and training:**

- [ ] Are prompts and responses logged by the AI provider?
- [ ] Is the organisation's data used to train models?
- [ ] Is an enterprise plan in use that provides data protection guarantees?

**Integrations:**

- [ ] Do any AI integrations have access to email, documents, or internal systems?
- [ ] Are API keys or credentials included in prompts or shared with AI tools?
- [ ] Do AI browser extensions have access to sensitive pages?

**Staff awareness:**

- [ ] Do staff know which AI tools are approved?
- [ ] Do staff know what they must not share with AI tools?

## Output format

Return:

- Exposure risk level: low, medium, or high
- Key risks identified
- Recommended changes
- Safer alternatives where applicable
- Open questions

## Anti-patterns

Avoid:

- assuming enterprise plans automatically protect all data without checking the specific terms
- focusing only on approved tools and missing the shadow AI problem
- giving generic “be careful with AI” advice without identifying specific risks
- treating this as a one-time audit rather than an ongoing concern
- ignoring AI browser extensions and third-party integrations as data exposure surfaces

## Disclaimer

This is a practical review tool, not legal advice, security certification, or compliance certification.
