---
name: ai-rag-privacy-review
description: Review a retrieval-augmented generation (RAG) system for privacy risks including document permission scoping, embedding exposure, over-retrieval, and access control. Use when building or auditing an internal AI assistant backed by documents or a vector database.
---

# AI RAG Privacy Review

## Purpose

Review a RAG system to check whether it respects document permissions, limits what it retrieves, and avoids leaking sensitive content through AI responses.

## Thinking style

Act as a defensive developer and architecture reviewer.

Focus on:

- whether permissions set at ingestion time are actually enforced at retrieval time
- what sensitive documents are in the index that should not be there
- what a determined user could retrieve by crafting their queries carefully

## Discovery questions

Ask:

1. What documents are indexed — are any HR files, legal documents, or customer records included?
2. Who can query the system, and does everyone have the same access level?
3. Are document-level permissions enforced at query time or only at ingestion?
4. Is document content sent to a third-party AI provider for embedding or generation?
5. What happens when a document is deleted from the source — is it removed from the index?

## Workflow

1. Identify what documents or data sources are indexed.
2. Check who can query the system and what they can retrieve.
3. Review whether document-level permissions are enforced at retrieval time.
4. Check what data is stored in the vector database.
5. Identify risks of over-retrieval or indirect data leakage.

## Checklist

**Document ingestion:**

- [ ] What documents are indexed (internal wikis, HR files, contracts, customer data)?
- [ ] Are all documents appropriate to index, or should some be excluded?
- [ ] Are documents chunked in a way that could expose partial sensitive content?

**Permissions and access control:**

- [ ] Are document-level access permissions enforced at retrieval time?
- [ ] Can a user retrieve documents they would not normally have access to?
- [ ] Is the retrieval scoped to the user's role or team?

**Vector database:**

- [ ] What data is stored in embeddings?
- [ ] Who has access to the vector database directly?
- [ ] Can raw document chunks be extracted from the database?

**AI responses:**

- [ ] Can the AI be prompted to reveal documents outside the user's scope?
- [ ] Do AI responses include sensitive data that should not be surfaced?
- [ ] Are responses logged, and if so where and for how long?

**Third-party AI services:**

- [ ] Is document content sent to a third-party AI provider for embedding or generation?
- [ ] Does the AI provider use the content for model training?

## Output format

Return:

- Risk level: low, medium, or high
- Key risks identified
- Recommended access control changes
- Indexing and scoping recommendations
- Open questions

## Anti-patterns

Avoid:

- treating ingestion-time access checks as equivalent to query-time access controls
- assuming the AI will refuse to surface restricted documents without testing this
- ignoring the third-party embedding provider as a data sharing step
- overlooking deletion — removing a document from the source does not remove its embeddings
- focusing only on direct queries and missing indirect extraction through AI responses

## Disclaimer

This is a practical review tool, not legal advice, security certification, or compliance certification.
