---
name: form-privacy-check
description: Review a form, survey, or sign-up flow for unnecessary or risky data collection. Use when designing or auditing a form that asks for personal information, contact details, or sensitive data.
---

# Form Privacy Check

## Purpose

Review a form to check whether it asks for more information than needed, whether sensitive fields are handled safely, and whether the purpose of each field is clear.

## Thinking style

Act as a plain-language privacy advisor.

Focus on:

- whether each field is genuinely necessary or just convenient to collect
- what happens to submissions after the form is completed
- whether the person filling in the form understands what their data will be used for

## Discovery questions

Ask:

1. What is the form for, and who fills it in?
2. Where do form submissions go — a spreadsheet, a database, an email inbox?
3. Who has access to the submitted responses?
4. Does the form collect information about children or other vulnerable groups?
5. Is there a privacy notice linked from the form?

## Workflow

1. List every field in the form.
2. For each field, ask: why is this needed and what happens if it is left blank?
3. Check whether any fields are sensitive (health, financial, ID numbers, age for children).
4. Check whether the form explains how the data will be used.
5. Recommend a leaner version.

## Checklist

- [ ] Does every field have a clear reason for being included?
- [ ] Are required fields actually necessary, or can some be optional?
- [ ] Does the form collect any sensitive information (health, financial, government IDs)?
- [ ] Does the form collect information about children?
- [ ] Is there a free-text field that might invite oversharing?
- [ ] Does the form explain what the data will be used for?
- [ ] Does the form explain who will see the data?
- [ ] Is there a privacy notice or link to one?
- [ ] Is the form transmitted securely (HTTPS)?
- [ ] Where is the submitted data stored, and who can access it?
- [ ] How long is the data kept?

## Output format

Return:

- List of fields reviewed
- Fields that should be removed or made optional
- Fields with sensitive data handling concerns
- Missing privacy notice or consent statement
- Recommended leaner version of the form
- Open questions

## Anti-patterns

Avoid:

- reviewing only the form fields and ignoring what happens to responses after submission
- treating optional fields as automatically low-risk — they still collect data when filled in
- assuming a privacy notice elsewhere on the site covers this form
- ignoring free-text fields that may capture more than intended
- recommending field removal without considering whether the form owner depends on it

## Disclaimer

This is a practical review tool, not legal advice, compliance certification, or a formal privacy impact assessment.
