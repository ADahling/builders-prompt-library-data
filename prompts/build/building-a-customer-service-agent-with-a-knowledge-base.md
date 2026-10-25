---
title: "Building a Customer Service Agent with a Knowledge Base"
slug: building-a-customer-service-agent-with-a-knowledge-base
stage: Build
category: "AI Agent Development"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/building-a-customer-service-agent-with-a-knowledge-base
---
# Building a Customer Service Agent with a Knowledge Base

Get a Python script for a customer service RAG agent that indexes private documents and uses LangChain retrieval to answer questions.

Variables: docs_path, user_question

## Prompt

Create a customer service AI agent that can answer questions based on a private knowledge base of documents. This is a common use case for Retrieval-Augmented Generation (RAG).

**System Components:**

1.  **Knowledge Base:** A collection of text documents (e.g., product manuals, FAQs, policy documents) located in a directory: `{{docs_path}}`.
2.  **Vector Store:** You will use a vector store (like FAISS or Chroma) to store the embeddings of the knowledge base documents.
3.  **Embedding Model:** Use an embedding model (e.g., `OpenAIEmbeddings`) to convert the documents into vectors.
4.  **Retriever:** Create a retriever from the vector store that can find the most relevant documents for a given user query.
5.  **LLM:** A conversational LLM (`ChatOpenAI`) to generate the final answer.
6.  **Chain:** Use LangChain's `RetrievalQA` chain to tie everything together.

**Workflow:**

1.  **Indexing (one-time setup):**
    *   Load the documents from the `{{docs_path}}`.
    *   Split the documents into smaller chunks.
    *   Generate embeddings for each chunk and store them in the vector store.
2.  **Querying (real-time):**
    *   When a user asks a question, the retriever finds the most relevant document chunks from the vector store.
    *   These chunks are passed to the LLM along with the user's question.
    *   The LLM uses the provided context to generate an answer.

**Your Task:**

Write a Python script that implements this RAG-based agent. The script should include both the indexing and querying logic.

**Input:**

*   `{{docs_path}}`: The path to the directory containing the knowledge base files.
*   `{{user_question}}`: The question from the user.

**Output:**

The agent's answer, grounded in the provided documents.
