---
title: "Store and search embeddings with pgvector"
slug: store-and-search-embeddings-with-pgvector
stage: Build
category: "LLM & AI Integration"
grade: A
score: 87
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/store-and-search-embeddings-with-pgvector
---
# Store and search embeddings with pgvector

Design a pgvector schema and search function with owner isolation, HNSW indexing, model dimensions, and safe content refreshes.

Variables: schema_definition, embedding_model_details, content_samples, search_requirements

## Prompt

You are a PostgreSQL engineer building embedding storage and search with pgvector.

Context:
- Existing schema and database versions: {{schema_definition}}
- Embedding model specifications: {{embedding_model_details}}
- Representative source content: {{content_samples}}
- Search, ownership, and refresh requirements: {{search_requirements}}

Your task is to design chunk storage, indexed similarity search, and safe re-embedding when content changes.

Steps:
1. Define token-based chunk boundaries, overlap, and stable chunk identifiers from the content. Respect model input limits and preserve source locations.
2. Design document and chunk tables with owner IDs, foreign keys, chunk text, content hashes, model version, and vector(d). Match d to the model. Check pgvector type and HNSW dimension limits; reject mixed embedding spaces.
3. Provide CREATE EXTENSION and migration SQL. For cosine search, use an HNSW index with vector_cosine_ops. Explain m, ef_construction, and query-time hnsw.ef_search choices. Reject zero vectors and dimension mismatches.
4. Write a match function taking a query vector, result limit, and similarity threshold. Return chunk IDs, text, and 1 - cosine distance. Use ORDER BY embedding <=> query_vector ASC and LIMIT for index eligibility. Apply the threshold as distance <= 1 - threshold; validate inputs.
5. Enforce owner scope with RLS and SECURITY INVOKER. Resolve identity through the supplied trusted auth mechanism, not an unchecked owner argument. Explain filtered HNSW underfilling, version-dependent iterative scans, and exact-search fallback.
6. Specify hash-based change detection, queued retries, idempotent writes, stale-job rejection, and atomic replacement of chunk sets. Keep old and new model versions separate. Provide EXPLAIN (ANALYZE, BUFFERS), recall comparisons against exact search, and cross-owner, threshold, and refresh checks.

Constraints:
- Do not invent project facts. List assumptions and unresolved inputs.
- Label SQL requiring missing version or auth details; do not claim execution.
- Never expose partially refreshed documents or compare incompatible models.

Output format, in Markdown: Assumptions, Chunking plan, Schema and index SQL, Match function and RLS SQL, Refresh workflow, and Verification table.

## Tips

Paste your existing schema, model name and dimensions, and representative source content. Include how owners are authenticated, expected search volume, and any PostgreSQL or pgvector version limits.
