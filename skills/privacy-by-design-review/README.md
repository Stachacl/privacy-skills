# Privacy by Design Review

Review a project, feature, product, or workflow against privacy-by-design principles to build better defaults before launch rather than fixing problems later.

## When to use this

- You are planning a new product or feature and want to check privacy risks before building starts.
- You are preparing for a product launch and want a practical early review.
- You want to apply privacy-by-design thinking without commissioning a full formal assessment.

## The checklist

1. Confirm there is a clear, specific purpose for collecting the data.
2. Check that only the minimum data necessary is being collected.
3. Check whether data is collected directly from the person or from a third party.
4. Check whether people know their data is being collected and have a way to opt out or request deletion.
5. Check who can access the data and whether access is limited to those who need it.
6. Check whether default settings are the most privacy-protective option, requiring opt-in rather than opt-out.
7. Check how long data is kept and whether there is an automatic deletion or anonymisation process.
8. Check whether deletion propagates to backups, caches, and third-party systems.
9. Check what data is shared with external services (analytics, AI, cloud providers).
10. Check whether AI is involved in processing or making decisions about personal data.
11. Check whether application logs contain personal data.
12. Check whether data is encrypted in transit and at rest.

## Examples

- A new customer feedback feature is reviewed before build and it is discovered that every free-text response is sent to a third-party analytics service.
- A product defaults to sharing usage data with the vendor. The privacy review changes this to opt-in.
- A deletion flow is added to the backlog before launch after the review reveals that deleting a user account does not remove data from the reporting database.

## Related skills

- [Data Minimisation Review](../data-minimisation-review/README.md)
- [Privacy Risk Review](../privacy-risk-review/README.md)
- [Privacy Impact Assessment Starter](../privacy-impact-assessment-starter/README.md)

## Related questions

- [Does our API return too much data?](../../docs/developers/does-our-api-return-too-much-data.md)
- [Are we logging PII?](../../docs/developers/are-we-logging-pii.md)
- [How do embeddings expose sensitive documents?](../../docs/developers/how-do-embeddings-expose-sensitive-documents.md)

## Not legal advice

This is a practical review tool, not legal advice, compliance certification, or a formal privacy impact assessment.

## About

Created by [Berrysbay Labs](https://www.berrysbay.com) as part of an open-source effort to make privacy thinking more practical for teams building with AI, cloud tools, and sensitive data.

Berrysbay Labs focuses on AI data exposure, local-first and on-prem AI systems, and tools that help reduce sensitive information before it leaves a device or organisation.
