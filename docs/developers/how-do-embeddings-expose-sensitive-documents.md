# How do embeddings expose sensitive documents?

## Short answer

When you embed documents into a vector database, the original content does not disappear — it is encoded in the embedding vectors, and the text chunks used to create them are usually stored alongside. Anyone with access to the database can retrieve document chunks directly. The AI system can also surface sensitive content to users who would not normally have access if permission filtering is not applied at query time.

## What to check

1. Check what documents have been embedded: are any of them sensitive (HR files, board minutes, contracts, salary data, health records)?
2. Check whether all indexed documents should be accessible to all users of the system, or whether only some users should see some documents.
3. Check whether document-level access permissions are enforced when a query is run — not just when documents are ingested.
4. Check whether the raw text chunks stored alongside embeddings contain personal data or sensitive content.
5. Check whether the embedding metadata includes author names, email addresses, or other identifying information.
6. Check whether someone with direct database access can retrieve raw document chunks without going through the AI interface.
7. Check whether the AI can be prompted to surface content from documents outside the querying user's scope.
8. Check whether there is a process to delete a document's embeddings if the source document is deleted or updated.
9. Check who has access to the vector database directly.
10. Check whether document content is sent to a third-party embedding or AI provider, and what their data terms say.

**Key risk patterns:**

- All documents indexed into a single shared namespace with no permission filtering
- Metadata stored alongside vectors includes original author and document path
- Deleted source documents leave orphaned embeddings in the vector store
- A RAG system that retrieves and surfaces content without checking whether the user is allowed to see it

## Use this skill

[Vector Database Privacy Check](../../skills/vector-database-privacy-check/README.md) — audit vector stores and embeddings for privacy and access risks.

[AI RAG Privacy Review](../../skills/ai-rag-privacy-review/README.md) — full review of a RAG system including retrieval permissions and AI response risks.

[Prompt Injection Privacy Review](../../skills/prompt-injection-privacy-review/README.md) — check whether adversarial inputs could extract sensitive content from the system.

## Related questions

- [Are we logging PII?](are-we-logging-pii.md)
- [Does our API return too much data?](does-our-api-return-too-much-data.md)
- [Can I upload this to an AI tool?](../everyday/can-i-upload-this-to-ai.md)

## Not legal advice

This is a practical review tool, not legal advice, security certification, or compliance certification.
