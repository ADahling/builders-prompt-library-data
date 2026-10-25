---
title: "Embedding Models: Generating Text Embeddings with SentenceTransformers"
slug: embedding-models-generating-text-embeddings-with-sentencetransformers
stage: Build
category: "LLM & AI Integration"
grade: A
score: 84
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/embedding-models-generating-text-embeddings-with-sentencetransformers
---
# Embedding Models: Generating Text Embeddings with SentenceTransformers

Generate vector embeddings for semantic search using the Python SentenceTransformers library and the all-MiniLM-L6-v2 pre-trained model.

## Prompt

You are building a semantic search feature and have decided to use an open-source model for generating embeddings to have more control and potentially lower costs. The 'SentenceTransformers' library is a popular choice for this.

Your task is to write a Python script that uses the 'sentence-transformers' library to generate embeddings for a set of sentences. This script will serve as a foundational component for your search system.

**Input Sentences:**
- "What are the best practices for API security?"
- "How do I implement OAuth2 in a web application?"
- "A guide to writing clean code."

**Technical Requirements:**
- The script must first ensure the 'sentence-transformers' library is installed (you can add a comment about the pip install command).
- Load a pre-trained model suitable for general-purpose semantic search, such as 'all-MiniLM-L6-v2'.
- The script should then call the model's 'encode' method with the list of input sentences.
- Finally, for each sentence, print the shape of the resulting embedding vector (e.g., (384,)) to confirm that the embeddings were generated correctly.

**Output Format:**
A single, runnable Python script that demonstrates how to generate embeddings using SentenceTransformers.
