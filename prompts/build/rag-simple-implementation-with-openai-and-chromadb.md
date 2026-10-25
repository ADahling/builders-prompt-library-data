---
title: "RAG: Simple Implementation with OpenAI and ChromaDB"
slug: rag-simple-implementation-with-openai-and-chromadb
stage: Build
category: "LLM & AI Integration"
grade: A
score: 89
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/rag-simple-implementation-with-openai-and-chromadb
---
# RAG: Simple Implementation with OpenAI and ChromaDB

Build a Python-based RAG pipeline using ChromaDB and OpenAI to answer queries strictly from a private knowledge base via vector retrieval.

## Prompt

Act as a developer tasked with building a basic Retrieval-Augmented Generation (RAG) system. This system will answer questions based on a small, private knowledge base, preventing the LLM from using its general knowledge.

Your goal is to create a Python script that orchestrates the RAG pipeline: retrieve relevant documents from a vector store (ChromaDB) and then pass them to an LLM (OpenAI) as context to answer a user's question.

**Knowledge Base:**
- "The company's standard support hours are 9 AM to 5 PM, Monday to Friday."
- "To reset your password, click the 'Forgot Password' link on the login page."
- "Our flagship product, the 'Innovator 3000', was launched in May 2023."

**User Question:**
"When can I contact support?"

**Technical Requirements:**
1.  **Setup:** Use 'openai', 'chromadb', and 'sentence-transformers' libraries.
2.  **Embedding and Storage:**
    - Generate embeddings for the knowledge base documents using 'all-MiniLM-L6-v2'.
    - Store these in a ChromaDB collection.
3.  **Retrieval:**
    - Generate an embedding for the user's question.
    - Query the ChromaDB collection to find the most relevant document (top_k=1).
4.  **Augmentation and Generation:**
    - Construct a new prompt for the OpenAI Chat Completions API.
    - This prompt must include the retrieved document as context and then ask the model to answer the user's original question based *only* on that context.
    - Example prompt structure: "Context: [retrieved document text]

Question: [user question]

Answer based only on the context provided."
5.  **Output:** Call the OpenAI API with this augmented prompt and print the model's final answer.

**Output Format:**
A single, end-to-end Python script implementing this simple RAG workflow.
