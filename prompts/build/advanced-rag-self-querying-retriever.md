---
title: "Advanced RAG: Self-Querying Retriever"
slug: advanced-rag-self-querying-retriever
stage: Build
category: "LLM & AI Integration"
grade: B
score: 74
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/advanced-rag-self-querying-retriever
---
# Advanced RAG: Self-Querying Retriever

Architect a self-querying RAG system that uses LLMs to convert natural language into structured metadata filters for precise retrieval.

## Prompt

Act as an AI engineer designing a sophisticated RAG system that can translate a user's natural language query into a structured query with metadata filters, without needing explicit instructions.

Your task is to design the logic for a 'Self-Querying Retriever'. This retriever uses an LLM to parse a user's query, extract the core question, and identify any metadata filters mentioned.

**Your Task: Design the Pseudocode/Logic**

**Scenario:**
- **Vector Store:** Contains movie summaries.
- **Metadata per document:** 'genre' (e.g., 'sci-fi', 'comedy'), 'year' (e.g., 1999), 'director' (e.g., 'James Cameron').
- **User Query:** "I want to watch a sci-fi movie directed by Christopher Nolan from after the year 2010."

**Logic Requirements:**

1.  **Step 1: Define Metadata Schema:**
    -   Clearly define the available metadata fields and their types (e.g., genre: string, year: int) for the LLM.

2.  **Step 2: The Self-Query LLM Call:**
    -   Construct a prompt for an LLM (e.g., GPT-5).
    -   The prompt must contain:
        -   The user's query.
        -   The metadata schema you defined.
        -   An instruction to act as a query parser.
        -   The instruction: "Extract the core search query and any metadata filters from the user's request. The core query should be what the user is actually asking about the content. The filters should be a structured object. If a filter is not present, do not include it."
        -   Specify the output format as a JSON object with two keys: 'query' (string) and 'filter' (object).

3.  **Step 3: Parse the LLM Output:**
    -   The LLM should return a JSON object like:
      `{
        "query": "a movie",
        "filter": {
          "genre": "sci-fi",
          "director": "Christopher Nolan",
          "year": { "gt": 2010 }
        }
      }`

4.  **Step 4: Execute the Structured Query:**
    -   Use the 'query' from the JSON to generate a query embedding.
    -   Use the 'filter' object to construct the metadata filter for your vector database (e.g., the 'where' clause in ChromaDB or the 'filter' parameter in Pinecone).
    -   Execute the similarity search with both the query embedding and the metadata filter.

5.  **Step 5: Generate Final Answer:**
    -   Pass the retrieved documents to a generator LLM to get the final answer.

**Output Format:**
Provide a detailed, step-by-step description of this self-querying process. Explain how this makes the RAG system more powerful and user-friendly.
