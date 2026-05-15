---
name: privacy-impact-assessment-starter
description: Create a lightweight privacy impact assessment starter for projects, workflows, tools, or systems. Use when a team needs an early privacy review before launching or changing a process.
---

# Privacy Impact Assessment Starter

## Purpose

Help a team complete a lightweight, practical privacy impact assessment (PIA) before launching a new project, system, tool, or workflow that involves personal data.

This is a starter, not a full DPIA. It helps teams identify risks early, not produce a compliance document.

## Thinking style

Act as a governance helper and privacy reviewer.

Focus on:

- understanding the project before jumping to risks
- asking questions the team may not have thought to ask
- helping the team produce something they will actually act on

## Discovery questions

Ask:

1. What is the project, tool, or change being reviewed?
2. What personal data is involved — who does it relate to, and what type?
3. Is this a new system, a change to an existing one, or a new use of existing data?
4. What is the purpose of collecting or using the data?
5. Has the team already identified any privacy concerns?

## Workflow

1. Document the project scope and purpose.
2. Identify the personal data involved and who it relates to.
3. Map where data is collected, stored, shared, and deleted.
4. Identify risks using the checklist below.
5. Recommend mitigations and identify unresolved questions for specialist review.

## PIA structure

**Section 1: Project overview**

- What is being built or changed?
- What is it for?

**Section 2: Data involved**

- What personal data is collected or used?
- Whose data is it (customers, employees, students, children, patients)?
- Is any data sensitive (health, financial, legal, biometric)?

**Section 3: Data flows**

- Where does data come from?
- Where is it stored?
- Who can access it?
- Is it shared with third parties or AI tools?

**Section 4: Risks identified**

- What could go wrong?
- What is the likelihood and impact?

**Section 5: Mitigations**

- What changes reduce the risk?
- What is still unresolved?

**Section 6: Sign-off and review date**

## Checklist

- [ ] Is there a clear lawful reason for using this data?
- [ ] Is only the minimum data necessary being collected?
- [ ] Are people told their data is being used?
- [ ] Is access limited to those who need it?
- [ ] Is data encrypted in transit and at rest?
- [ ] Is there a retention and deletion plan?
- [ ] Are any third parties or AI tools involved?
- [ ] Is there a plan for a data breach or incident?
- [ ] Does any automated decision-making affect people?

## Output format

Return:

- Draft PIA with all sections filled in based on the information provided
- Gaps or unanswered questions
- Risks identified and suggested mitigations
- Items requiring specialist legal or security review
- Recommended next step

## Anti-patterns

Avoid:

- treating this as a compliance checkbox rather than a genuine risk review
- completing the PIA without speaking to the people building or using the system
- marking risks as mitigated without confirming mitigations are actually in place
- producing a document that no one will read or act on
- assuming a short or small project does not need a review

## Disclaimer

This is a lightweight practical starter, not a formal Data Protection Impact Assessment (DPIA), legal advice, or compliance certification. Some projects may require a full DPIA under applicable data protection law.
