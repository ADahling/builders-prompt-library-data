---
title: "RAG Pipeline Architecture"
slug: rag-pipeline-architecture
stage: Build
category: "LLM & AI Integration"
grade: A+
score: 92
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/rag-pipeline-architecture
---
# RAG Pipeline Architecture

Architect a production-ready RAG pipeline tailored to specific document types, performance targets, and retrieval strategies.

Variables: use_case, document_types, corpus_size, max_latency, accuracy_target

## Prompt

You are an AI engineer. Design a production-grade RAG (Retrieval-Augmented Generation) pipeline for {{use_case}}.

Requirements:
- Document types: {{document_types}}
- Corpus size: {{corpus_size}}
- Query latency: <{{max_latency}} seconds
- Accuracy target: {{accuracy_target}}

Design:
1. **Document Processing**: Chunking strategy (size, overlap, semantic boundaries)
2. **Embedding Model**: Model selection (OpenAI, Cohere, open-source) with justification
3. **Vector Store**: Database selection (Pinecone, Weaviate, pgvector) with indexing strategy
4. **Retrieval Strategy**: Hybrid search (semantic + keyword), re-ranking, MMR diversity
5. **Context Assembly**: How to combine retrieved chunks into a coherent context
6. **Prompt Engineering**: System prompt with retrieved context, citation instructions
7. **Evaluation**: Metrics (faithfulness, relevance, answer correctness), evaluation dataset
8. **Guardrails**: Hallucination detection, source attribution, confidence scoring
9. **Caching**: Query cache, embedding cache, response cache
10. **Monitoring**: Retrieval quality metrics, latency tracking, cost tracking

## Tips

RAG is the most practical way to give LLMs access to your private data. The chunking strategy makes or breaks it.
