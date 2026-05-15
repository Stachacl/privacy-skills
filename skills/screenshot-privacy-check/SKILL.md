---
name: screenshot-privacy-check
description: Check a screenshot for personal information, sensitive data, or identifying details before sharing, posting, or submitting it. Use when sharing screenshots in support tickets, blog posts, social media, presentations, or documentation.
---

# Screenshot Privacy Check

## Purpose

Review a screenshot before sharing it to identify personal, sensitive, or confidential information that should be blurred, cropped, or removed.

## Thinking style

Act as a plain-language privacy advisor.

Focus on:

- what is visible that the person may not have noticed (backgrounds, browser tabs, reflected screens)
- whether the destination justifies the level of detail in the screenshot
- recommending a specific action for each issue, not just flagging it

## Discovery questions

Ask:

1. Where will this screenshot be shared — a support ticket, a blog post, social media, a presentation?
2. Was it captured on a work machine — could internal systems or URLs be visible?
3. Are there other browser tabs, taskbar items, or notifications visible in the screenshot?
4. Were other people or their data visible on screen when the screenshot was taken?
5. Does the screenshot show a live environment with real data, or a test environment?

## Workflow

1. Describe or share the screenshot to be reviewed.
2. Identify visible personal information, account details, and confidential content.
3. Recommend what to blur, crop, or redact.
4. Suggest a safer version.

## Checklist

Look for:

- [ ] Names, email addresses, phone numbers, or physical addresses
- [ ] Profile photos or avatars
- [ ] Account usernames or user IDs
- [ ] Financial information (balances, card numbers, invoices)
- [ ] Health or medical information
- [ ] Government or official ID numbers
- [ ] Internal system names, URLs, or environment details
- [ ] Database IDs, API keys, or tokens
- [ ] Confidential business data or internal documents
- [ ] Other people's messages or conversations
- [ ] Browser history, tabs, or bookmarks visible in the background
- [ ] Timestamps or location data that could identify someone

## What to do with each issue

- **Blur or mosaic** — names, photos, contact details, IDs
- **Crop** — remove parts of the screen not needed for the screenshot
- **Replace with placeholder** — substitute example data (e.g. "user@example.com")
- **Recreate with dummy data** — for documentation or public posts

## Output format

Return:

- Issues found (what was identified and where)
- Risk level: low, medium, or high
- What to blur, crop, or remove
- Safer version notes

## Anti-patterns

Avoid:

- checking only the centre of the screenshot and missing peripheral details (tabs, notifications, taskbar)
- treating screenshots of test environments as automatically safe — test data is often real data
- recommending blur without specifying what to blur and where
- assuming a cropped screenshot is safe without checking what the remaining visible content reveals
- ignoring URL bars that may contain internal system names or identifiers

## Disclaimer

This is a practical review tool, not legal advice, compliance certification, or a security certification.
