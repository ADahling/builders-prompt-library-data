---
title: "RAG: Advanced Implementation with Metadata Filtering"
slug: rag-advanced-implementation-with-metadata-filtering
stage: Build
category: "LLM & AI Integration"
grade: A
score: 84
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/rag-advanced-implementation-with-metadata-filtering
---
# RAG: Advanced Implementation with Metadata Filtering

Implement a Python script using ChromaDB to perform a RAG query with metadata filtering to ensure search results are specific to a source.

## Prompt

You are enhancing a RAG system to handle more complex queries. The system needs to filter documents based on metadata *before* performing the similarity search. This is useful for scenarios where a user wants to search within a specific source or time frame.

Your task is to write a Python script using ChromaDB that demonstrates metadata filtering in a query.

**Scenario:**
- **Documents & Metadata:**
    1.  Text: "The project alpha_docs.pdf details the initial project scope.", Metadata: {'source': 'project_alpha'}
    2.  Text: "The project beta_docs.pdf covers the revised timeline.", Metadata: {'source': 'project_beta'}
    3.  Text: "General onboarding information is in onboarding.pdf.", Metadata: {'source': 'general'}
    4.  Text: "The scope for project beta is to build a new dashboard.", Metadata: {'source': 'project_beta'}
- **User Query:** "What is the timeline?"
- **Filter:** The user only wants to search within documents related to 'project_beta'.

**Technical Requirements:**
- Use 'chromadb' and 'sentence-transformers'.
- Create a ChromaDB collection and add the four documents with their corresponding embeddings and metadata.
- The user's query is "What is the timeline?". Generate an embedding for this query.
- Perform a query against the collection using the 'collection.query()' method.
- Crucially, the query must include a 'where' clause to filter for documents where the 'source' metadata field is equal to 'project_beta'. The filter would be: `where={"source": "project_beta"}`.
- Request the top 1 result.
- The script should print the text of the retrieved document. The expected result is "The project beta_docs.pdf covers the revised timeline.", not the document from project_alpha, even if it were semantically similar.

**Output Format:**
A complete Python script demonstrating a RAG query with metadata filtering.
