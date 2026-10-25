---
title: "Vector Databases: Performing a Similarity Search in ChromaDB"
slug: vector-databases-performing-a-similarity-search-in-chromadb
stage: Build
category: "LLM & AI Integration"
grade: A
score: 84
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/vector-databases-performing-a-similarity-search-in-chromadb
---
# Vector Databases: Performing a Similarity Search in ChromaDB

Get a Python script that embeds sample documents in ChromaDB and retrieves the top two matches to demonstrate RAG similarity search.

## Prompt

You have a ChromaDB collection populated with document embeddings. Now, you need to implement the core functionality of a RAG system: retrieving documents relevant to a user's query.

Your task is to write a Python script that performs a similarity search (or query) against a ChromaDB collection. The script will first populate the database and then query it to find the most relevant documents for a given question.

**Setup:**
1.  **Documents to store:**
    - "The 2020 Summer Olympics were held in Tokyo, Japan."
    - "The capital of France is Paris, known for the Eiffel Tower."
    - "The main components of a computer are the CPU, RAM, and storage."
2.  **Query:** "What is the famous landmark in Paris?"

**Technical Requirements:**
- Use the 'chromadb' and 'sentence-transformers' libraries.
- Create an in-memory ChromaDB collection.
- Use the 'all-MiniLM-L6-v2' model from SentenceTransformers to generate embeddings for both the documents and the query.
- Add the documents and their embeddings to the collection.
- Use the 'collection.query()' method to search the collection. The query should use the embedding of the user's question.
- Request the top 2 most similar documents.
- The script must print the 'documents' field from the query result, which contains the text of the retrieved documents.

**Output Format:**
A single, executable Python script that demonstrates the query process.
