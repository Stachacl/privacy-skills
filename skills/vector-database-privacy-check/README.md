# Vector Database Privacy Check

Review vector databases, embeddings, indexes, and semantic search systems for privacy, access control, retention, deletion, and sensitive data exposure risks.

## When to use this

- You are building or auditing a RAG system or semantic search tool backed by a vector database.
- You want to check whether sensitive documents stored as embeddings could be exposed or reconstructed.
- You are reviewing access control and deletion capabilities in a vector store.

## The checklist

1. Identify what documents or content has been embedded and stored in the vector database.
2. Check whether all stored content is appropriate, or whether some documents should have been excluded.
3. Check who can query the vector database and what they can retrieve.
4. Check whether document-level access permissions are enforced at query time.
5. Check whether raw document chunks or metadata stored alongside embeddings expose personal data.
6. Check whether embeddings can be used to approximately reconstruct the original document content.
7. Check who has direct access to the vector database (e.g. engineers, admins, the AI system).
8. Check whether there is a process to delete a specific document's embeddings if needed.
9. Check how long embeddings are retained.
10. Check whether the vector database is hosted by a third-party provider and what their data terms are.

## Examples

- An internal knowledge base indexes all HR documents into a shared vector store. An engineer with database access can retrieve chunks of salary reviews.
- A RAG system stores document metadata including the original author's name and email alongside embeddings. This metadata is returned in query results.
- A document deletion process removes the source file but does not remove the corresponding embeddings from the vector store.

## Related skills

- [AI RAG Privacy Review](../ai-rag-privacy-review/README.md)
- [Prompt Injection Privacy Review](../prompt-injection-privacy-review/README.md)
- [Architecture Privacy Review](../architecture-privacy-review/README.md)

## Related questions

- [How do embeddings expose sensitive documents?](../../docs/developers/how-do-embeddings-expose-sensitive-documents.md)
- [Are we logging PII?](../../docs/developers/are-we-logging-pii.md)
- [Does our API return too much data?](../../docs/developers/does-our-api-return-too-much-data.md)

## Not legal advice

This is a practical review tool, not legal advice, security certification, or compliance certification.

## Berrysbay support

For teams who want a guided review, [Berrysbay](https://www.berrysbay.com) can help.
