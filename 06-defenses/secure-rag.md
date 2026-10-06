# Secure RAG (Retrieval-Augmented Generation)

## Risks
Indirect prompt injection in documents, poisoned corpus, unauthorized retrieval, cross-tenant leakage, embedding inversion, stale or wrong data (misinformation).

## Ingestion pipeline controls
- [ ] Approved sources only; record provenance
- [ ] Scan documents (malware, hidden text, instructions)
- [ ] Classify sensitivity and attach metadata/ACLs to every chunk
- [ ] Review process for externally sourced content
- [ ] Versioning and ability to remove documents quickly

## Retrieval controls
- [ ] **Filter by user permissions at query time** (not after generation)
- [ ] Tenant-isolated indexes or namespaces
- [ ] Limit number and size of retrieved chunks
- [ ] Log what was retrieved for whom

## Generation controls
- [ ] Prompt marks retrieved text as untrusted data
- [ ] Output DLP and citation checks
- [ ] Refuse when no supporting sources found

## Vector store security
- Encrypt at rest/in transit, network isolation, authN/authZ, backups
- Treat embeddings as sensitive as source data

## Tests
- Ask for documents the user shouldn't see
- Insert a canary document containing a harmless injected instruction and see if it is followed
- Cross-tenant query tests
