---
title: "RAG Pipeline Prompt Template"
slug: rag-pipeline-prompt-template
stage: Build
category: "AI Agent Development"
grade: B
score: 75
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/rag-pipeline-prompt-template
---
# RAG Pipeline Prompt Template

Get a RAG prompt tailored to your documents and questions, with citation rules, chunking guidance, and retrieval tuning.

## Prompt

Design a Retrieval Augmented Generation (RAG) prompt for my [describe knowledge base / document set]:

1. RETRIEVAL CONTEXT TEMPLATE:
```
You are a helpful assistant that answers questions using ONLY the provided context. If the context doesn't contain enough information to answer, say "I don't have enough information to answer that" — do NOT make up answers.

## Retrieved Context
{context}

## User Question
{question}

## Instructions
- Answer based ONLY on the context above.
- Quote the specific passage that supports your answer.
- If multiple passages are relevant, synthesize them.
- If the context is contradictory, note the contradiction.
- Include the source document/section for each claim.
```

2. CHUNKING STRATEGY:
   - Optimal chunk size for your content type (500-1000 tokens for docs, shorter for FAQs)
   - Overlap between chunks (10-20%)
   - Metadata to attach: source, section, date, author

3. RETRIEVAL TUNING:
   - Number of chunks to retrieve (start with 5, adjust based on quality)
   - Similarity threshold (discard low-relevance results)
   - Re-ranking strategy for better relevance

4. HALLUCINATION PREVENTION:
   - Grounding instructions in the system prompt
   - Citation requirements
   - Confidence calibration

Customize for my specific use case: [describe your documents and expected questions].

## Tips

RAG is how you give AI access to your own data without fine-tuning. The prompt structure determines hallucination rates. Source: progress.com/blogs/mastering-the-art-of-prompting-llms-for-rag
