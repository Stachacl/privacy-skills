---
name: cloud-storage-sharing-check
description: Review cloud file and folder sharing for privacy, access, oversharing, and retention risks. Use when sharing files through Google Drive, OneDrive, Dropbox, SharePoint, iCloud, or similar cloud storage tools.
---

# Cloud Storage Sharing Check

## Purpose

Review cloud file and folder sharing settings to identify oversharing, unnecessary access, and retention risks before sharing links or granting access.

## Thinking style

Act as a plain-language privacy advisor.

Focus on:

- who actually needs access and who might inadvertently have it
- whether "anyone with the link" sharing creates risks
- what happens to access after the immediate need is over

## Discovery questions

Ask:

1. What platform is being used — Google Drive, OneDrive, Dropbox, SharePoint, or other?
2. What sharing setting is being used — specific people, anyone with the link, or public?
3. What does the file or folder contain — personal data, confidential information, or internal documents?
4. Who are the intended recipients — internal staff, external partners, or members of the public?
5. Is there a time limit on the share, or will access persist indefinitely?

## Workflow

1. Identify the platform and sharing setting.
2. Identify the content being shared and its sensitivity.
3. Check whether the sharing level is wider than needed.
4. Check retention — how long will access remain open?
5. Recommend tighter settings or a safer sharing method.

## Checklist

**Sharing settings:**

- [ ] Is the link set to "anyone with the link" when it should be restricted to specific people?
- [ ] Can recipients edit the file when they should only need to view it?
- [ ] Can recipients share the link with others?

**Access scope:**

- [ ] Does the share include a whole folder when only a single file is needed?
- [ ] Do all recipients need the same level of access?
- [ ] Are former employees, contractors, or partners still listed with access?

**Content sensitivity:**

- [ ] Does the file contain personal data (names, emails, health, financial)?
- [ ] Does it contain confidential business information?
- [ ] Is the folder at a higher level than intended, exposing other files?

**Retention and expiry:**

- [ ] Does the share have an expiry date?
- [ ] Will access be revoked after the task is complete?
- [ ] Are there old shares still active that should be closed?

**Platform-specific risks:**

- [ ] Is this a consumer account (personal Google/iCloud) rather than an enterprise account?
- [ ] Does the platform sync files locally to devices that could be lost or shared?

## Output format

Return:

- Risk level: low, medium, or high
- Issues found with sharing settings, access scope, or content
- Recommended changes to settings
- Safer sharing approach if applicable
- Open questions

## Anti-patterns

Avoid:

- treating "anyone with the link" as private because the link is long
- assuming access will be cleaned up later without a specific plan
- ignoring parent folder permissions when sharing a single file
- recommending platform-specific steps without checking which platform is in use
- assuming enterprise and consumer accounts have the same protections

## Disclaimer

This is a practical review tool, not legal advice, security certification, or compliance certification.
