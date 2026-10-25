---
title: "Advanced Embeddings: Visualizing Embeddings with PCA"
slug: advanced-embeddings-visualizing-embeddings-with-pca
stage: Build
category: "LLM & AI Integration"
grade: A+
score: 91
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/advanced-embeddings-visualizing-embeddings-with-pca
---
# Advanced Embeddings: Visualizing Embeddings with PCA

Generate a Python script to visualize high-dimensional sentence embeddings in a 2D PCA scatter plot to analyze semantic clusters.

## Prompt

As an ML engineer, you've generated high-dimensional embeddings for a set of documents. To understand the semantic relationships captured in these embeddings, you want to visualize them. Since you can't visualize 384 dimensions, you need to reduce them to 2 or 3 dimensions using a technique like Principal Component Analysis (PCA).

Your task is to write a Python script that generates embeddings, reduces their dimensionality using PCA, and creates a 2D scatter plot to visualize the result.

**Scenario:**
- **Input Sentences:** A list of sentences with clear semantic clusters.
    - "The cat is sleeping on the couch."
    - "My kitten loves to play with yarn."
    - "The sun is a star at the center of our solar system."
    - "The moon orbits the Earth."
    - "I need to write a Python script."
    - "Let's debug this code together."
- **Goal:** Create a plot where sentences about cats, space, and coding form distinct clusters.

**Technical Requirements:**
- Use the 'sentence-transformers', 'numpy', 'scikit-learn', and 'matplotlib' libraries.
- **Embedding:** Use 'all-MiniLM-L6-v2' to generate embeddings for the sentences.
- **Dimensionality Reduction:** Use `sklearn.decomposition.PCA` to reduce the embeddings from their original dimension down to 2 components.
- **Visualization:** Use `matplotlib.pyplot` to create a 2D scatter plot of the reduced embeddings.
- **Labeling:** Each point on the scatter plot should be annotated with its corresponding sentence (or a shortened version).
- The script should display the plot when run.

**Output Format:**
A complete Python script that generates and displays the 2D visualization of the sentence embeddings.
