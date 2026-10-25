---
title: "Building a Q&A Agent over a GitHub Repository"
slug: building-a-q-a-agent-over-a-github-repository
stage: Build
category: "AI Agent Development"
grade: A+
score: 90
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/building-a-q-a-agent-over-a-github-repository
---
# Building a Q&A Agent over a GitHub Repository

Get a Python script that indexes repository files in a vector database and equips an agent to retrieve code snippets for codebase questions.

Variables: repo_url

## Prompt

Create an AI agent that can answer questions about the codebase of a specific GitHub repository. This involves combining document loading, vector databases, and an agent framework.

**Workflow:**

1.  **Ingestion:**
    *   Clone the target repository: `{{repo_url}}`.
    *   Use LangChain's `GitLoader` or a combination of `DirectoryLoader` and `TextLoader` to load the code files (e.g., .py, .js, .md).
    *   Split the code into chunks using a `RecursiveCharacterTextSplitter` (consider using language-specific splitters if available).
    *   Embed the chunks and store them in a vector database (like Chroma).
2.  **Retrieval Tool:**
    *   Create a retriever from the vector database.
    *   Wrap this retriever in a tool called `search_codebase`. The tool should take a query string and return the most relevant code snippets.
3.  **Agent Setup:**
    *   Initialize a conversational agent (e.g., `ConversationalRetrievalAgent` or a custom ReAct agent).
    *   Give the agent the `search_codebase` tool.
    *   Provide a system prompt that instructs the agent to act as a senior developer familiar with the repository.

**Task:**

Ask the agent a specific question about the code, such as "Where is the authentication logic implemented?" or "Explain how the `process_data` function works."

**Output:**

A Python script that performs the ingestion (you can assume the repo is already cloned locally for simplicity) and sets up the agent to answer questions.
