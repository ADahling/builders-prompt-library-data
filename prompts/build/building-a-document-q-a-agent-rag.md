---
title: "Building a Document Q&A Agent (RAG)"
slug: building-a-document-q-a-agent-rag
stage: Build
category: "AI Agent Development"
grade: A+
score: 96
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/building-a-document-q-a-agent-rag
---
# Building a Document Q&A Agent (RAG)

Create a simple Retrieval-Augmented Generation RAG agent that can answer questions about a document you provide.

Variables: file_path, question

## Prompt

Create a simple Retrieval-Augmented Generation (RAG) agent that can answer questions about a document you provide. This is one of the most common and powerful use cases for LLMs.

**The Workflow:**

1.  **Load:** Load a document (e.g., a text file `{{file_path}}`).
2.  **Split:** Split the document into smaller, manageable chunks.
3.  **Store:** Embed the chunks and store them in a vector store (a simple in-memory one like FAISS is fine for this).
4.  **Retrieve:** When a user asks a question, search the vector store for the most relevant chunks.
5.  **Generate:** Pass the user's question and the retrieved chunks to an LLM to generate the final answer.

**Your Task (using LangChain):**

LangChain makes this easy.

1.  Use a `TextLoader` to load the document.
2.  Use a `RecursiveCharacterTextSplitter` to split it.
3.  Use `OpenAIEmbeddings` and a `FAISS` vector store.
4.  Create a `RetrievalQA` chain, which handles the retrieval and generation steps for you.

**Input:**

*   `{{file_path}}`: Path to a text file.
*   `{{question}}`: A question about the content of the file.

**Output:**

A complete Python script that sets up this RAG pipeline and answers a question.
