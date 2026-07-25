# Project Development Stages

## Stage 1: Project Foundation

Build the basic project setup.

* Initialize project with `uv`
* Add dependencies
* Create basic folder structure
* Add environment configuration
* Create FastAPI application
* Add health endpoint
* Connect PostgreSQL
* Add initial database migrations

---

## Stage 2: Document Management

Build basic document handling.

* Upload a document
* Store document metadata
* Generate a document ID
* Track document processing state
* Prevent obvious duplicate uploads
* Retrieve document details

---

## Stage 3: Document Parsing

Convert uploaded documents into structured content.

* Parse documents with Docling
* Extract Markdown
* Preserve headings and sections
* Capture page and source metadata
* Handle unsupported or invalid files

---

## Stage 4: Chunking

Split parsed content into usable chunks.

* Create basic structure-aware chunks
* Preserve document and section references
* Add chunk metadata
* Validate chunk size
* Prepare chunks for embedding

---

## Stage 5: Embeddings and Storage

Generate embeddings and store chunks.

* Generate embeddings with OpenAI
* Store chunks in PostgreSQL
* Store vectors using pgvector
* Store metadata
* Confirm all chunks are indexed

---

## Stage 6: Vector Retrieval

Build basic semantic search.

* Generate query embedding
* Search similar chunks
* Return top matching chunks
* Apply document filters
* Test retrieval quality

---

## Stage 7: Keyword Retrieval

Add PostgreSQL full-text search.

* Create text search indexes
* Search chunks using keywords
* Return ranked keyword results
* Test keyword matching

---

## Stage 8: Hybrid Retrieval

Combine vector and keyword search.

* Run both searches
* Merge results
* Remove duplicates
* Apply score fusion
* Return combined results

---

## Stage 9: Reranking

Improve retrieval quality.

* Send retrieved chunks to Cohere
* Rerank results
* Limit final chunks
* Handle reranker failures safely

---

## Stage 10: Context Building

Prepare retrieved information for the language model.

* Arrange ranked chunks
* Remove repeated content
* Control context size
* Create citation references
* Produce a final context bundle

---

## Stage 11: Answer Generation

Generate answers from retrieved context.

* Create a basic prompt
* Call `gpt-4o-mini`
* Return a validated answer
* Include citations
* Handle missing information

---

## Stage 12: Complete RAG API

Expose the complete workflow through FastAPI.

* Document upload endpoint
* Document details endpoint
* Query endpoint
* Ingestion endpoint
* Validation
* Basic error responses

---

## Stage 13: Testing and Stability

Test the complete system.

* Unit tests
* Database integration tests
* Ingestion tests
* Retrieval tests
* End-to-end query tests
* Fix critical bugs

---

## Stage 14: PydanticAI Agent

Add agent orchestration only after the basic RAG flow works.

* Create answer agent
* Add retrieval tool
* Add typed dependencies
* Return structured responses
* Keep retrieval logic outside the agent

---

## Stage 15: Advanced Improvements

Implement only when required.

* Background ingestion
* Caching
* Conversation memory
* Multi-agent workflows
* Multi-tenancy
* Advanced monitoring
* Performance optimization
* Deployment improvements
