# AI RAG Privacy Review

Review a retrieval-augmented generation (RAG) system to check whether it respects document permissions, limits what it retrieves, and avoids leaking sensitive content through AI responses.

## When to use this

- You are building or auditing an internal AI assistant backed by documents or a knowledge base.
- You want to check whether users can retrieve documents they should not have access to.
- You are reviewing a vector database or semantic search system for privacy risks.

## The checklist

1. Identify what documents or data sources are indexed in the system.
2. Check whether all indexed documents are appropriate to include, or whether some should be excluded.
3. Confirm that document-level access permissions are enforced at retrieval time, not just at ingest.
4. Check whether a user can query documents outside their role or team scope.
5. Review what data is stored in the vector database and who can access it directly.
6. Check whether raw document chunks can be extracted from the database.
7. Test whether the AI can be prompted to reveal documents outside the user's scope.
8. Check whether AI responses and retrieved chunks are logged, and for how long.
9. Check whether document content is sent to a third-party AI provider and whether that provider uses it for training.

## Examples

- A company builds an internal assistant using all company documents, including board minutes and salary information, without filtering by role.
- A developer discovers that embedding vectors can be decoded to approximate the original document content by anyone with database access.
- An AI assistant returns confidential HR information to a standard employee because the retrieval step does not check permissions.

## Related skills

- [Vector Database Privacy Check](../vector-database-privacy-check/README.md)
- [Architecture Privacy Review](../architecture-privacy-review/README.md)
- [Logging Privacy Review](../logging-privacy-review/README.md)

## Related questions

- [How do embeddings expose sensitive documents?](../../docs/developers/how-do-embeddings-expose-sensitive-documents.md)
- [Are we logging PII?](../../docs/developers/are-we-logging-pii.md)
- [Does our API return too much data?](../../docs/developers/does-our-api-return-too-much-data.md)

## Not legal advice

This is a practical review tool, not legal advice, security certification, or compliance certification.

## Berrysbay support

For teams who want a guided review, [Berrysbay](https://www.berrysbay.com) can help.
