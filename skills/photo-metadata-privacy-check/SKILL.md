---
name: photo-metadata-privacy-check
description: Review photos and images for hidden privacy risks including metadata, location, faces, documents, screens, uniforms, backgrounds, and identifying details. Use before posting or sharing photos online.
---

# Photo Metadata Privacy Check

## Purpose

Review photos and images for visible and hidden privacy risks before sharing, posting, or submitting them.

## Thinking style

Act as a plain-language privacy advisor.

Focus on:

- what is visible in the image that the person may not have noticed
- what metadata the file carries that is not visible but can be extracted
- whether identifiable people have consented to being in a public image

## Discovery questions

Ask:

1. Where will this photo be posted or shared — social media, a website, a report, a support ticket?
2. Are there people in the photo — did they consent to being in a public image?
3. Was the photo taken on a phone — is location data embedded in the file?
4. Are there any screens, documents, whiteboards, or notices visible in the background?
5. Are there uniforms, badges, office signage, or branding visible?

## Workflow

1. Identify the sharing destination and audience.
2. Check visible content: people, documents, screens, uniforms, backgrounds.
3. Check for embedded metadata: GPS location, device information, timestamps.
4. Identify what needs to be blurred, cropped, or stripped before sharing.
5. Recommend a safer version.

## Checklist

**Visible content:**

- [ ] Are identifiable people visible who have not consented to being in a public image?
- [ ] Are children visible?
- [ ] Are documents, screens, or whiteboards visible with readable text?
- [ ] Are badges, ID cards, or access passes visible?
- [ ] Is office signage, branding, or a specific location identifiable?
- [ ] Are home interiors or personal belongings visible?
- [ ] Are vehicle number plates visible?

**Metadata:**

- [ ] Does the image file contain GPS coordinates (common in phone photos)?
- [ ] Does the file contain device make/model or serial number?
- [ ] Does the file contain the original timestamp?
- [ ] Has metadata been stripped before sharing if location privacy matters?

**Context-specific risks:**

- [ ] Is this a photo from a school, healthcare, or care setting where stricter rules apply?
- [ ] Could the photo be used to identify someone’s home address or regular location?
- [ ] Is this a professional event photo — were attendees told photos would be taken?

## Output format

Return:

- Risk level: low, medium, or high
- Visible privacy risks identified
- Metadata risks identified
- What to blur, crop, or strip before sharing
- Safer sharing notes
- Open questions

## Anti-patterns

Avoid:

- assuming photos taken in public places are automatically safe to share online
- ignoring background details (screens, documents, notices)
- treating metadata as unimportant — GPS data in phone photos can reveal home addresses
- assuming people in photos have consented because they were present at an event
- recommending steps without checking whether the person has access to metadata-stripping tools

## Disclaimer

This is a practical review tool, not legal advice, security certification, or compliance certification.
