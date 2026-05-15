---
name: ai-upload-decision-check
description: Decide whether information is safe to paste, upload, or send to an AI tool. Use when reviewing customer data, internal documents, PDFs, contracts, screenshots, or personal information before using ChatGPT, Claude, Gemini, Copilot, or other AI tools.
---

# AI Upload Decision Check

## Purpose

Review the content before it is pasted, uploaded, or sent to an AI tool.

This skill helps decide whether the content is safe to share, needs changes first, or should not be uploaded at all.

## Thinking style

Act as a plain-language privacy advisor.

Focus on:

- what specific data is in the content and who it relates to
- whether the AI tool is consumer or enterprise — the distinction matters significantly
- whether redaction or generalisation actually makes the content safe enough to share

## Discovery questions

Ask:

1. What tool is being used — consumer (free ChatGPT, Gemini) or approved enterprise?
2. What is in the content — does it include names, customer data, or internal details?
3. What is the content being uploaded for — what task needs to be done?
4. Could the task be completed with a redacted or generalised version instead?
5. Does the organisation have an approved tool better suited for this use case?

## Workflow

1. Identify the AI tool being used and whether it is a consumer, enterprise, or local/on-prem tool.
2. Identify what is in the content: personal information, customer data, confidential business data, or internal documents.
3. Check whether the tool logs prompts, uses inputs for training, or shares data with third parties.
4. Decide whether redaction or generalisation is possible.
5. Give a final recommendation.

## Checklist

- [ ] Does the content include names, email addresses, phone numbers, or IDs?
- [ ] Does it include customer or client information?
- [ ] Does it include employee or HR information?
- [ ] Does it include financial details, contracts, or pricing?
- [ ] Does it include health, legal, or other sensitive information?
- [ ] Does it include internal system names, credentials, or architecture details?
- [ ] Does it include confidential business strategy?
- [ ] Is this a consumer AI tool (e.g. free ChatGPT, Gemini) or an approved enterprise tool?
- [ ] Could the content be redacted or generalised before uploading?
- [ ] Is there an approved enterprise or on-prem version of this tool available?

## Output format

Return:

- Content risk level: low, medium, or high
- What was identified in the content
- Specific items to remove or change before uploading
- Whether an approved enterprise or local tool is a better option
- Final recommendation: safe to upload / safe with changes / do not upload

## Anti-patterns

Avoid:

- assuming redacting a name is sufficient when other identifying details remain
- treating consumer and enterprise tools as equivalent based on brand name alone
- approving an upload without checking what the tool does with inputs
- giving a “safe with changes” recommendation without specifying exactly what to change
- ignoring context — a document safe for one tool may not be safe for another

## Disclaimer

This is a practical review tool, not legal advice, security certification, or compliance certification.
