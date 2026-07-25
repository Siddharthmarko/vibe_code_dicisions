# Development Rules

## Build Order

### Phase 1 - Foundation

* Project setup
* Configuration
* FastAPI
* PostgreSQL connection
* Database migrations
* Health API

---

### Phase 2 - Ingestion

* Upload document
* Parse with Docling
* Chunk document
* Generate embeddings
* Store in PostgreSQL

---

### Phase 3 - Retrieval

* Embed query
* Vector search
* Keyword search
* Hybrid search
* Cohere reranking

---

### Phase 4 - Answering

* Build context
* Generate answer
* Return citations

---

### Phase 5 - API

* Upload API
* Query API
* Document API
* Error handling

---

# Always Maintain

* Type safety (Pydantic)
* Clean module boundaries
* Thin API routes
* Async code
* Logging
* Error handling
* Database migrations
* Unit tests
* Integration tests

---

# Highest Priority

Keep this pipeline working at all times.

```text
Document
   ↓
Parse
   ↓
Chunk
   ↓
Embed
   ↓
Store
   ↓
Retrieve
   ↓
Rerank
   ↓
Context
   ↓
Answer
```

---

# Build Later

* Agents
* Multi-agent workflows
* Memory
* Cache
* Background jobs
* Multi-tenancy
* Performance optimization
* Advanced monitoring

---

# Rules

* Build one feature at a time.
* Finish it before starting the next.
* Keep the project runnable after every change.
* Don't create unnecessary abstractions.
* Don't duplicate models.
* Keep business logic out of API routes.
* Isolate third-party libraries inside adapters.
* Refactor only when needed.
* Every commit should be deployable.
