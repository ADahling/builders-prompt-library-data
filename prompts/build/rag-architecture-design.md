---
title: "RAG Architecture Design"
slug: rag-architecture-design
stage: Build
category: "LLM & AI Integration"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/rag-architecture-design
---
# RAG Architecture Design

Design a RAG system for your knowledge sources with chunking, retrieval, grounding, evaluation, caching, and per-query cost estimates.

## Prompt

Design a Retrieval-Augmented Generation (RAG) system for this use case:

Use case: [what users will ask, what knowledge base to search]
Data sources: [documents, databases, APIs]
Volume: [number of documents, average size]
Update frequency: [how often does source data change]

Design:
1. Chunking strategy: How to split documents? (fixed size, semantic, recursive?) Chunk size and overlap?
2. Embedding model: Which model? Dimensions? Cost per 1K tokens?
3. Vector store: Which database? (Pinecone, pgvector, Weaviate, Chroma) Why?
4. Retrieval: Top-k? Re-ranking? Hybrid search (keyword + semantic)?
5. Context window management: How to fit retrieved chunks + user query + system prompt within token limit?
6. Prompt template: System prompt that grounds the LLM on retrieved context.
7. Hallucination mitigation: Citation format, "I don't know" handling, confidence scoring.
8. Evaluation: How to measure retrieval quality (recall@k) and answer quality?
9. Caching: Cache frequent queries? Invalidation strategy?
10. Cost: Estimated cost per query (embedding + LLM inference).

## Tips

RAG is the most common LLM integration pattern — get the architecture right first.
