---
title: "Advanced Embeddings: Cosine Similarity Calculation"
slug: advanced-embeddings-cosine-similarity-calculation
stage: Build
category: "LLM & AI Integration"
grade: A+
score: 91
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/advanced-embeddings-cosine-similarity-calculation
---
# Advanced Embeddings: Cosine Similarity Calculation

Get a Python script that embeds sample sentences and calculates cosine similarity from scratch with NumPy to compare semantic similarity.

## Prompt

You have generated vector embeddings for two pieces of text and want to measure how semantically similar they are. The standard way to do this is by calculating the cosine similarity between their embedding vectors.

Your task is to write a Python script that generates embeddings for two sentences and then calculates the cosine similarity between them from scratch using NumPy.

**Scenario:**
- **Sentence 1:** "The cat is sleeping."
- **Sentence 2:** "My kitten is taking a nap."
- **Sentence 3:** "I am eating a sandwich."

**Goal:** Show that the similarity between Sentence 1 and 2 is high, and the similarity between Sentence 1 and 3 is low.

**Technical Requirements:**
- Use 'sentence-transformers' and 'numpy'.
- **Step 1 (Embed):** Use a model like 'all-MiniLM-L6-v2' to generate embeddings for the three sentences.
- **Step 2 (Calculate Similarity):** Write a Python function `cosine_similarity(vec1, vec2)` that takes two NumPy arrays.
    -   Inside the function, calculate the dot product of the two vectors.
    -   Calculate the L2 norm (magnitude) of each vector.
    -   The cosine similarity is the dot product divided by the product of the norms.
- **Step 3 (Compare):**
    -   Call your function to calculate the similarity between the embeddings of Sentence 1 and Sentence 2.
    -   Call it again to calculate the similarity between Sentence 1 and Sentence 3.
- **Step 4 (Output):** Print the two similarity scores. The first should be close to 1.0, and the second should be much lower.

**Output Format:**
A complete Python script that demonstrates the calculation.
