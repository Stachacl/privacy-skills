---
name: architecture-privacy-review
description: Review a system or software architecture for privacy risks including data flows, third-party dependencies, storage, access control, and logging. Use when assessing a new or existing technical architecture before build, launch, or audit.
---

# Architecture Privacy Review

## Purpose

Review a system architecture to identify where personal or sensitive data is handled, stored, or exposed, and whether controls are appropriate.

## Thinking style

Act as an architecture reviewer.

Focus on:

- mapping data flows through the system, not just the main path
- identifying where data accumulates in logs, caches, queues, and exports
- checking whether third-party dependencies have access to more data than intended

## Discovery questions

Ask:

1. What is the system’s main purpose, and what personal data is central to it?
2. What third-party services, APIs, or cloud providers does it depend on?
3. Are there any async systems — queues, event streams, or batch jobs — that carry personal data?
4. What is logged and where do logs go?
5. Are there admin tools or internal dashboards that expose personal data?

## Workflow

1. Identify the components in the architecture (services, databases, APIs, third-party tools).
2. Map which components handle personal or sensitive data.
3. Review data flows between components.
4. Check access controls, encryption, and logging.
5. Identify gaps and recommend changes.

## Checklist

**Data flows:**

- [ ] Where does personal data enter the system?
- [ ] Which services or components handle personal data?
- [ ] Is personal data passed between services unnecessarily?
- [ ] Is personal data sent to third-party services or APIs?

**Storage:**

- [ ] Where is personal data stored (databases, caches, queues, files, logs)?
- [ ] Is data encrypted at rest?
- [ ] Are backups encrypted and access-controlled?

**Access control:**

- [ ] Which services or people can access personal data?
- [ ] Are there role-based access controls in place?
- [ ] Are internal admin tools protected from external access?

**Encryption and transit:**

- [ ] Is data encrypted in transit between services?
- [ ] Are internal service-to-service calls encrypted?

**Logging:**

- [ ] Do logs contain personal data?
- [ ] Are log access controls in place?

**Third-party dependencies:**

- [ ] What third-party services or libraries handle personal data?
- [ ] Are data processing agreements in place with vendors?

## Output format

Return:

- Risk level: low, medium, or high
- Key privacy risks by component or data flow
- Recommended changes
- Safer architecture alternatives where applicable
- Open questions

## Anti-patterns

Avoid:

- reviewing only the primary data flow and missing logs, caches, queues, and exports
- assuming third-party dependencies are safe without checking what data they receive
- treating encryption at rest as a complete privacy control
- skipping the admin and internal tooling review — it is often the weakest point
- producing a risk list without recommending specific architectural changes

## Disclaimer

This is a practical review tool, not legal advice, security certification, or compliance certification.
