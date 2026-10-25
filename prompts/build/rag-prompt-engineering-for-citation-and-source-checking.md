---
title: "RAG: Prompt Engineering for Citation and Source-Checking"
slug: rag-prompt-engineering-for-citation-and-source-checking
stage: Build
category: "LLM & AI Integration"
grade: A
score: 80
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/rag-prompt-engineering-for-citation-and-source-checking
---
# RAG: Prompt Engineering for Citation and Source-Checking

Write a multi-part RAG prompt for answering a system features question using labeled context documents and citations for each claim.

## Prompt

In a production RAG system, it's critical that the LLM's answers are grounded in the retrieved documents and that the system can provide citations. This builds user trust and allows for verification.

Your task is to create a prompt for an LLM that forces it to answer a question based on several provided context documents and to cite the source for each piece of information it uses.

**Scenario:**
- **User Question:** "What are the key features and limitations of the new system?"
- **Retrieved Documents (Context):**
    - **[SOURCE 1: design_doc.txt]** "The new system features a real-time analytics dashboard, role-based access control, and a REST API for integrations. It is built on a microservices architecture."
    - **[SOURCE 2: user_manual.txt]** "Users can create custom reports and export data in CSV or PDF formats. The dashboard is accessible on mobile devices."
    - **[SOURCE 3: limitations.txt]** "The current version does not support single sign-on (SSO). The API has a rate limit of 100 requests per minute."

**Prompt Engineering Task:**
Construct a detailed, multi-part prompt to be sent to a powerful LLM (like GPT-5 or Claude Opus 4.8). This is a text-based task. You are not writing code, but the prompt itself.

**Prompt Requirements:**
1.  **Introduction:** Start by clearly stating the user's question.
2.  **Context Provision:** Provide the retrieved documents, each clearly labeled with a source identifier (e.g., "[SOURCE 1: design_doc.txt]").
3.  **Core Instruction:** Instruct the model to synthesize an answer to the user's question using *only* the provided documents.
4.  **Citation Mandate:** Explicitly require the model to cite the source identifier (e.g., `[SOURCE 1]`) immediately after every piece of information it presents. Multiple citations are allowed if information is combined.
5.  **Handling Missing Information:** Instruct the model that if the answer cannot be found in the documents, it must state exactly that and not use its own knowledge.
6.  **Output Format:** Specify that the final output should be a well-structured paragraph, not a list.

**Output Format:**
Provide a single block of text representing the complete, final prompt that would be sent to the LLM.
