---
name: data-minimisation-review
description: Review a system, service, or dataset to identify where more personal data is being collected, stored, or shared than is necessary. Use when auditing data collection practices, simplifying a data model, or preparing for a privacy review.
---

# Data Minimisation Review

## Purpose

Review what personal data is being collected and retained to identify what can be reduced, anonymised, or removed.

## Thinking style

Act as a privacy reviewer.

Focus on:

- whether each data field has a genuine, current use or is collected out of habit
- how retention compounds the problem — data not deleted accumulates risk over time
- recommending a leaner data model that still meets the business need

## Discovery questions

Ask:

1. What system, service, or dataset is being reviewed?
2. Is this triggered by a specific concern, or a general review?
3. When was this data model last reviewed for necessity?
4. Are there any fields collected historically that are no longer actively used?
5. Is there a retention policy in place, or does data accumulate indefinitely?

## Workflow

1. List the personal data fields or datasets being collected.
2. For each field or dataset, ask: why is this needed?
3. Identify what can be removed, aggregated, or replaced with a less specific version.
4. Review retention: is data kept longer than necessary?
5. Recommend a leaner data model.

## Checklist

**Collection:**

- [ ] Why is each field or dataset collected?
- [ ] Is there a field that is collected but rarely or never used?
- [ ] Could a less specific version be used (e.g. age range instead of date of birth)?
- [ ] Are free-text fields encouraging oversharing?

**Storage:**

- [ ] Is data stored in multiple places unnecessarily?
- [ ] Are old records retained beyond their useful life?
- [ ] Are test or demo records stored alongside production data?

**Sharing:**

- [ ] Is full personal data shared with third parties when only a subset is needed?
- [ ] Are analytics or reporting tools receiving more data than necessary?

**Retention:**

- [ ] Is there a retention policy?
- [ ] Is data automatically deleted or anonymised after a defined period?

## Output format

Return:

- Risk level: low, medium, or high
- Fields or datasets that can be removed or reduced
- Retention gaps identified
- Recommended leaner data model
- Open questions

## Anti-patterns

Avoid:

- accepting “we might need it later” as a reason to keep collecting a field
- treating data minimisation as removing only obviously sensitive fields
- ignoring free-text fields that invite users to over-share
- recommending removal without checking whether anything depends on the field
- treating a one-off review as a complete solution without a retention policy

## Disclaimer

This is a practical review tool, not legal advice, compliance certification, or a formal privacy impact assessment.
