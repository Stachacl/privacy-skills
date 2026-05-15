---
name: privacy-risk-review
description: Identify and rate privacy risks in a project, process, system, or planned change. Use when assessing risks before making a decision, launching a product, onboarding a vendor, or making a change that involves personal data.
---

# Privacy Risk Review

## Purpose

Review a project, system, or planned change to identify privacy risks, rate their severity, and recommend mitigations.

## Thinking style

Act as a privacy reviewer.

Focus on:

- identifying risks that are specific to this project, not generic risks that apply to everything
- rating risks by likelihood and impact, not just by category
- recommending mitigations that are practical given the team’s constraints

## Discovery questions

Ask:

1. What is the project, system, or change being reviewed?
2. What personal data is involved, and whose data is it?
3. What is the timeline — is this pre-build, mid-build, or pre-launch?
4. Are there any risks the team has already identified?
5. Are there third-party services, AI tools, or integrations involved?

## Workflow

1. Describe the project, system, or change being reviewed.
2. Identify what personal or sensitive data is involved.
3. Identify potential risks using the checklist below.
4. Rate each risk: low, medium, or high.
5. Recommend mitigations.

## Checklist

**Data exposure:**

- [ ] Could personal data be accessed by unauthorised people?
- [ ] Could data be exposed through a security weakness?
- [ ] Could data be shared with the wrong person or system?

**Over-collection:**

- [ ] Is more data being collected than is needed?
- [ ] Is data retained longer than necessary?

**Consent and transparency:**

- [ ] Do people know their data is being collected or used?
- [ ] Is there a lawful basis for collection and processing?

**Third-party risks:**

- [ ] Is personal data shared with vendors, partners, or AI tools?
- [ ] Are third parties trusted and covered by agreements?

**AI and automation:**

- [ ] Is personal data used in AI training or automated decisions?
- [ ] Could AI outputs expose or infer personal information?

**Incidents:**

- [ ] What would happen if this data were lost, stolen, or leaked?
- [ ] Is there a plan for responding to a data breach?

## Output format

Return:

- List of risks identified
- Risk rating per item: low, medium, or high
- Overall risk level
- Recommended mitigations
- Open questions

## Anti-patterns

Avoid:

- rating all risks as medium to avoid difficult conversations
- producing a risk list with no mitigations or owners
- treating third-party and AI risks as lower priority than first-party risks
- completing the review without input from the people building or running the system
- treating low probability as equivalent to low impact — low-probability, high-impact risks still need mitigations

## Disclaimer

This is a practical review tool, not legal advice, compliance certification, or a formal data protection impact assessment.
