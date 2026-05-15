---
name: ai-meeting-notes-check
description: Review AI meeting notes, transcripts, summaries, and recordings for privacy and confidentiality risks. Use when using AI note-takers, meeting bots, Zoom, Teams, Google Meet, Otter, Fireflies, or similar tools.
---

# AI Meeting Notes Check

## Purpose

Review the use of AI tools for meeting transcription, notes, and summaries to identify consent gaps, confidentiality risks, and unsafe storage or sharing practices.

## Thinking style

Act as a plain-language privacy advisor.

Focus on:

- whether meeting participants knew an AI tool was present
- what sensitive content was captured that should not be stored or shared
- where the transcript or recording ends up and who can access it

## Discovery questions

Ask:

1. Which AI tool was used — Otter, Fireflies, Copilot, Zoom AI, or another?
2. Did all participants know an AI note-taker was present before the meeting started?
3. What was discussed — were any personal, HR, client, legal, or health matters covered?
4. Where are the transcript and recording stored, and who can access them?
5. Does the tool use meeting content for model training?

## Workflow

1. Identify the tool and whether it is an approved enterprise service or a consumer tool.
2. Check whether all participants consented to being recorded or transcribed.
3. Review what sensitive content was captured.
4. Check storage location, access controls, and retention.
5. Recommend actions for safe handling or deletion.

## Checklist

**Consent and notice:**

- [ ] Were all participants told an AI note-taker would be present?
- [ ] Were external participants (clients, candidates, students) told?
- [ ] Did anyone object — was the tool removed or turned off?
- [ ] Is recording consent required in this context (e.g. HR, legal, school)?

**Tool and vendor:**

- [ ] Is this an approved enterprise tool or a consumer service?
- [ ] Does the tool use recordings or transcripts to train AI models?
- [ ] Does the vendor store recordings — for how long?
- [ ] Where is data stored (jurisdiction, cloud region)?

**Content captured:**

- [ ] Were personal details about individuals discussed?
- [ ] Were HR, performance, or employment matters discussed?
- [ ] Were client or customer details discussed?
- [ ] Were health, legal, or financial matters discussed?
- [ ] Was confidential business strategy discussed?

**Storage and access:**

- [ ] Where is the transcript or recording stored?
- [ ] Who has access to it?
- [ ] Has it been shared more widely than intended?
- [ ] Is there a retention limit?

## Output format

Return:

- Risk level: low, medium, or high
- Consent gaps identified
- Sensitive content captured that requires care
- Storage and access risks
- Recommended actions (delete, restrict access, re-consent)
- Open questions

## Anti-patterns

Avoid:

- assuming consent because no one objected during the meeting
- treating AI-generated summaries as less sensitive than full transcripts
- ignoring external participants who may have stricter expectations
- assuming enterprise tools are automatically safe without checking training and retention terms
- recommending generic "review your settings" without specific steps

## Disclaimer

This is a practical review tool, not legal advice, security certification, or compliance certification.
