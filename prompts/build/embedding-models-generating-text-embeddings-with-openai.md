---
title: "Embedding Models: Generating Text Embeddings with OpenAI"
slug: embedding-models-generating-text-embeddings-with-openai
stage: Build
category: "LLM & AI Integration"
grade: A
score: 84
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/embedding-models-generating-text-embeddings-with-openai
---
# Embedding Models: Generating Text Embeddings with OpenAI

Generate batch text embeddings using OpenAI's Python API and the text-embedding-3-small model to power semantic search applications.

## Prompt

As a machine learning engineer, you need to convert a list of documents into numerical representations (embeddings) for use in a semantic search system.

Your task is to write a Python script that uses the OpenAI Embeddings API to generate vector embeddings for a batch of text documents.

**Input Documents:**
- "The sky is blue."
- "The sun is bright."
- "An apple a day keeps the doctor away."
- "Software engineering is a fascinating field."

**Technical Requirements:**
- Use the 'openai' Python library.
- Use a modern and cost-effective embeddings model, such as 'text-embedding-3-small'.
- The script should take the list of input documents and send them to the embeddings API in a single batch request.
- It must then iterate through the response, and for each document, print the first 5 dimensions of its corresponding embedding vector to the console.
- Include comments in your script explaining how to access the embeddings from the API response object.
- Ensure the API key is managed securely via an environment variable.

**Output Format:**
A complete, executable Python script that prints the truncated embeddings for each document.
