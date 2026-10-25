---
title: "Vector Databases: Storing Embeddings in ChromaDB"
slug: vector-databases-storing-embeddings-in-chromadb
stage: Build
category: "LLM & AI Integration"
grade: B
score: 78
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/vector-databases-storing-embeddings-in-chromadb
---
# Vector Databases: Storing Embeddings in ChromaDB

Generate a Python script to initialize an in-memory ChromaDB collection and store text documents with custom embeddings and metadata.

## Prompt

As an AI developer building a Retrieval-Augmented Generation (RAG) system, you have generated embeddings for your document corpus. The next step is to store these embeddings in a vector database for efficient similarity searching.

Your task is to write a Python script that demonstrates how to store text documents and their corresponding embeddings in ChromaDB, a popular open-source vector database.

**Scenario:**
- **Documents:** ["The cat sat on the mat.", "The dog chased the ball.", "Photosynthesis is the process used by plants."]
- **Embeddings:** You will generate dummy embeddings for this exercise. For example, [[0.1, 0.2, ...], [0.3, 0.4, ...], [0.5, 0.6, ...]].
- **Metadata:** Each document should have a 'source' metadata field (e.g., 'doc1.txt', 'doc2.txt').
- **IDs:** Each entry needs a unique ID (e.g., "id1", "id2").

**Technical Requirements:**
- Use the 'chromadb' Python library.
- Create an in-memory ChromaDB client (persistent client is not needed for this example).
- Create a new collection named 'document_collection'.
- Add the documents, their dummy embeddings, metadata, and IDs to the collection using the 'collection.add()' method.
- After adding the data, perform a 'collection.peek()' to retrieve a sample of the stored items and print it to the console to verify the operation was successful.

**Output Format:**
A complete Python script that shows the end-to-end process of adding data to a ChromaDB collection.
