---
title: "Vector Database Selection & RAG Architecture"
slug: vector-database-selection-rag-architecture
stage: Build
category: "Modern Data Stack"
grade: A+
score: 96
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/vector-database-selection-rag-architecture
---
# Vector Database Selection & RAG Architecture

Compare vector database options by application, data volume, query load, and hosting needs when planning a RAG or semantic search system.

Variables: app, docs, tokens, qps, frequency, hosting

## Prompt

# Vector Database Selection & RAG Architecture

## Use Case Assessment
- Application: {{app}} (semantic search / chatbot / recommendation / image similarity)
- Data volume: {{docs}} documents, ~{{tokens}} tokens average
- Query volume: {{qps}} queries/second
- Update frequency: {{frequency}} (static corpus / daily / real-time)
- Hosting preference: {{hosting}} (managed / self-hosted / embedded)

## Vector Database Comparison (March 2026)

| Database | Type | Best For | Pricing Model |
|----------|------|----------|---------------|
| **pgvector** (Supabase) | Extension on Postgres | Existing Postgres users, <1M vectors | Part of Supabase plan |
| **Pinecone** | Managed cloud | Production scale, zero ops | Per-vector + per-query |
| **Weaviate** | Open source / cloud | Multi-modal (text + image), GraphQL | Self-host free, cloud paid |
| **Chroma** | Embedded / cloud | Prototyping, Python-native | Open source, cloud paid |
| **Qdrant** | Open source / cloud | High performance, filtering | Self-host free, cloud paid |
| **Milvus/Zilliz** | Open source / cloud | Massive scale (billions) | Self-host free, cloud paid |
| **Turbopuffer** | Cloud | Cost-effective at scale | Storage-based pricing |

### pgvector with Supabase (Recommended Start)
```sql
-- Enable vector extension
CREATE EXTENSION IF NOT EXISTS vector;

-- Create embeddings table
CREATE TABLE documents (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  content TEXT NOT NULL,
  metadata JSONB DEFAULT '{}',
  embedding VECTOR(1536)  -- OpenAI ada-002 dimension
);

-- Create HNSW index for fast similarity search
CREATE INDEX ON documents 
  USING hnsw (embedding vector_cosine_ops)
  WITH (m = 16, ef_construction = 64);

-- Similarity search function
CREATE OR REPLACE FUNCTION match_documents(
  query_embedding VECTOR(1536),
  match_threshold FLOAT DEFAULT 0.78,
  match_count INT DEFAULT 5
) RETURNS TABLE (id UUID, content TEXT, metadata JSONB, similarity FLOAT)
LANGUAGE sql STABLE AS $$
  SELECT id, content, metadata, 
    1 - (embedding <=> query_embedding) AS similarity
  FROM documents
  WHERE 1 - (embedding <=> query_embedding) > match_threshold
  ORDER BY embedding <=> query_embedding
  LIMIT match_count;
$$;
```

## Embedding Model Selection
| Model | Dimensions | Cost (per 1M tokens) | Quality |
|-------|-----------|----------------------|---------|
| OpenAI text-embedding-3-small | 1536 | $0.02 | Good |
| OpenAI text-embedding-3-large | 3072 | $0.13 | Best |
| Cohere embed-v4 | 1024 | $0.10 | Very good |
| Google text-embedding-005 | 768 | Free (limited) | Good |
| Open source (BGE, E5) | 384-1024 | Self-host | Varies |

## Chunking Strategy
| Method | Chunk Size | Overlap | Best For |
|--------|-----------|---------|----------|
| Fixed-size | 512-1024 tokens | 50-100 | General purpose |
| Semantic | Variable | None | Well-structured documents |
| Recursive | 512-1024 tokens | 50 | Code, markdown |
| Sentence-based | 3-5 sentences | 1 sentence | Conversational content |

## Production Checklist
- [ ] Embedding pipeline handles updates (upsert, not just insert)
- [ ] Metadata filtering reduces search space before vector similarity
- [ ] Hybrid search: combine vector similarity with keyword search (BM25)
- [ ] Re-ranking: use cross-encoder to re-rank top-k results
- [ ] Caching: cache frequent query embeddings
- [ ] Monitoring: track query latency, recall quality, cache hit rate
- [ ] Cost controls: batch embedding generation, rate limit queries

## Tips

Vector database comparison with pgvector/Supabase implementation, embedding model selection, chunking strategies, and production checklist for RAG systems.
