---
name: vector-database-privacy-check
description: Review vector databases, embeddings, indexes, and semantic search systems for privacy, access control, retention, deletion, and sensitive data exposure risks. Use when building or auditing RAG and AI search systems.
---

# Vector Database Privacy Check

## Purpose

Review a vector database or embedding-based search system to identify what sensitive data is stored in embeddings, who can retrieve it, and whether deletion and access controls are in place.

## Thinking style

Act as a defensive developer.

Focus on:

- what personal or sensitive data is encoded in the embeddings
- whether access controls at the document level are enforced at retrieval time
- whether deletion is genuinely possible — embeddings are not obviously deletable

## Discovery questions

Ask:

1. What documents or data were chunked and embedded — what types of content do they contain?
2. Who can query the vector database, and is retrieval scoped to a user’s permissions?
3. Can a user retrieve content from documents they would not normally have access to?
4. Is there a way to delete a specific document’s embeddings if the source document is deleted?
5. Who has direct database access, and can they extract raw chunks?

## Workflow

1. Identify what is indexed and what sensitive data it contains.
2. Check access controls at query time.
3. Check whether retrieval is scoped to the user’s permissions.
4. Check deletion and retention: what happens when a document is removed from the source?
5. Check direct database access and monitoring.

## Checklist

**What is indexed:**

- [ ] What types of documents are in the index (HR files, legal documents, customer records, internal wikis)?
- [ ] Does the index contain personal data, confidential content, or access-controlled documents?
- [ ] Were documents checked for appropriateness before being indexed?
- [ ] Are documents chunked in a way that could surface sensitive partial content?

**Access control at retrieval:**

- [ ] Is retrieval scoped to the user’s role or permissions?
- [ ] Can a user retrieve chunks from a document they would not normally have access to?
- [ ] Are document-level ACLs enforced at query time, not just at ingestion?

**Deletion:**

- [ ] If a source document is deleted, are its embeddings also removed from the index?
- [ ] Is there a tested process for removing a specific document’s embeddings on request?
- [ ] Are there orphaned embeddings from deleted source documents?

**Direct database access:**

- [ ] Who has direct access to the vector database?
- [ ] Can raw document chunks be extracted from the database by admins?
- [ ] Is database access logged and monitored?

**Third-party embedding services:**

- [ ] Is content sent to a third-party service to generate embeddings?
- [ ] Does that service use content for model training?

## Output format

Return:

- Risk level: low, medium, or high
- Data types identified in the index
- Access control gaps
- Deletion and retention risks
- Direct access risks
- Recommended changes
- Open questions

## Anti-patterns

Avoid:

- assuming embeddings are anonymous — they encode document content and can be used to reconstruct it
- treating ingestion-time access checks as equivalent to query-time access checks
- ignoring deletion — “delete the source document” does not automatically remove embeddings
- assuming small indexes do not need access controls
- overlooking the third-party embedding provider as a data sharing risk

## Disclaimer

This is a practical review tool, not a security certification, penetration test, or compliance certification.
