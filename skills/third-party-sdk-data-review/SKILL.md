---
name: third-party-sdk-data-review
description: Review third-party SDKs, packages, analytics tools, widgets, and integrations for privacy, tracking, data sharing, and supply-chain risks. Use when adding external code or services to an app or website.
---

# Third Party SDK Data Review

## Purpose

Review a third-party SDK, analytics tool, widget, or integration before adding it to an application or website to identify what data it collects, where it sends it, and what risks it introduces.

## Thinking style

Act as a defensive developer.

Focus on:

- what data the SDK can access once included in the app or page
- where that data goes and whether the organisation controls it
- whether the vendor’s data collection is proportionate to what the SDK is needed for

## Discovery questions

Ask:

1. What is the SDK or tool being added, and what is it needed for?
2. What data will it have access to — page content, user IDs, device details, network requests?
3. Where does the SDK send data — to a vendor server, third-party analytics, or ad networks?
4. Is there a privacy policy or developer documentation describing what data is collected?
5. Is this SDK well-maintained and widely used, or a niche tool with limited scrutiny?

## Workflow

1. Identify the SDK and its stated purpose.
2. Check what data it accesses (network, device, user, page content).
3. Check where data is sent and to whom.
4. Check the vendor’s data retention and training use policies.
5. Assess supply-chain risk: is this a well-maintained, trusted package?

## Checklist

**Data access:**

- [ ] What data does the SDK access (cookies, local storage, user IDs, DOM content, network requests)?
- [ ] Does it have access to personal data the user has entered on the page?
- [ ] Does it fingerprint the device or browser?
- [ ] Does it read or write cookies across domains?

**Data sharing:**

- [ ] Does the SDK send data to the vendor’s servers?
- [ ] Does it share data with advertising networks, data brokers, or other third parties?
- [ ] Is the data shared named in the vendor’s privacy policy?
- [ ] Does the vendor use data for their own analytics or model training?

**Consent and user notice:**

- [ ] Does including this SDK require disclosing it in the privacy policy?
- [ ] Does it require user consent (e.g. cookie consent under GDPR/ePrivacy)?
- [ ] Is there a way to conditionally load it only after consent?

**Supply-chain and security:**

- [ ] Is this a well-maintained, reputable package?
- [ ] Is the package pinned to a specific version or hash to prevent supply-chain attacks?
- [ ] Has the package had known vulnerabilities in the past?

**Data processing agreement:**

- [ ] Is there a DPA or data processing terms with the vendor?

## Output format

Return:

- Risk level: low, medium, or high
- Data collected by the SDK
- Data sharing and vendor use identified
- Consent requirements
- Supply-chain risks
- Recommended changes or alternatives
- Open questions

## Anti-patterns

Avoid:

- assuming a popular SDK is safe because many others use it
- ignoring consent requirements because the SDK “only uses analytics”
- adding SDKs without reviewing what access they actually need
- assuming removing an SDK stops its data collection if it has already set cookies or fingerprinted users
- skipping the DPA check because the vendor is well-known

## Disclaimer

This is a practical review tool, not legal advice, security certification, or compliance certification.
