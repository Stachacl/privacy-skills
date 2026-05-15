# Data Flow Mapping

Trace where personal or sensitive data enters, moves through, is stored, and exits a system or workflow to understand where it goes and who can access it.

## When to use this

- You are preparing for a privacy review or audit and need to map what data the system handles.
- You are building a new system and want to understand the data flows before adding controls.
- You need to answer "where does our customer data actually go?" for a vendor, auditor, or regulator.

## The checklist

1. Identify the system, workflow, or process being mapped.
2. List where data enters: forms, uploads, APIs, integrations, manual entry, or imports.
3. Trace how data moves through the system: services, databases, queues, event streams.
4. Identify where data is stored and for how long at each stage.
5. Check whether data is transformed or enriched at any point, and whether new fields are added.
6. Identify where data exits: exports, vendor sharing, logs, AI tools, or public output.
7. Note access controls at each stage.
8. Identify any gaps in retention or deletion processes.

## Examples

- A customer support system receives tickets via email, stores them in a CRM, sends summaries to a third-party AI tool, and logs requests to a cloud logging service — but only the CRM storage was known to the privacy team.
- A data mapping exercise reveals that marketing analytics tools receive user IDs that can be combined with other data to identify individuals.
- A mapping exercise shows that data is retained indefinitely in a backup database that the deletion process does not reach.

## Related skills

- [Architecture Privacy Review](../architecture-privacy-review/README.md)
- [Data Minimisation Review](../data-minimisation-review/README.md)
- [Logging Privacy Review](../logging-privacy-review/README.md)

## Related questions

- [Are we logging PII?](../../docs/developers/are-we-logging-pii.md)
- [Does our API return too much data?](../../docs/developers/does-our-api-return-too-much-data.md)
- [How do embeddings expose sensitive documents?](../../docs/developers/how-do-embeddings-expose-sensitive-documents.md)

## Not legal advice

This is a practical review tool, not legal advice, compliance certification, or a formal data protection impact assessment.

## Berrysbay support

For teams who want a guided review, [Berrysbay](https://www.berrysbay.com) can help.
