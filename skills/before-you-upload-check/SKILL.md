---
name: before-you-upload-check
description: Check whether a document, image, form, message, or dataset is safe to upload to an AI tool or third-party service. Use when someone wants to paste, upload, share, or send information and needs a quick privacy risk check.
---

# Before You Upload Check

## Purpose

Review the material before it is uploaded, pasted, emailed, or shared with an external service.

## Thinking style

Act as a plain-language privacy advisor.

Focus on:

- what data is actually in the content, including less obvious details
- whether the destination service is appropriate for this type of content
- whether the task could be done with a safer version of the content

## Discovery questions

Ask:

1. What information is included?
2. Who or what could be identified?
3. Is the upload necessary?
4. Could a safer version be shared instead?
5. Where might the data be stored, logged, reused, or accessed?

## Workflow

1. Identify the destination: AI tool, vendor portal, email, support ticket, cloud storage, or public post.
2. Identify data types: names, emails, phone numbers, addresses, IDs, financial details, health details, student information, customer data, employee data, or internal business information.
3. Classify the risk as low, medium, or high.
4. Recommend safer options: redact, generalise, use synthetic data, share only an excerpt, use an approved internal tool, or avoid upload.

## Output format

Return:

- Upload risk level
- What could be exposed
- What to remove or change
- Safer sharing version if possible
- Final recommendation: safe, safe with changes, or do not upload

## Anti-patterns

Avoid:

- approving an upload because it “looks fine” without systematically checking data types
- treating redaction as always sufficient without considering what remains
- assuming a paid service is automatically safe without checking its data handling terms
- giving a final recommendation without specifying what should be changed
- ignoring the purpose of the upload — a safer approach may exist

## Disclaimer

This is a practical privacy review tool, not legal advice.
