---
title: "Advanced Embeddings: Topic Modeling with Top2Vec"
slug: advanced-embeddings-topic-modeling-with-top2vec
stage: Build
category: "LLM & AI Integration"
grade: A
score: 82
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/advanced-embeddings-topic-modeling-with-top2vec
---
# Advanced Embeddings: Topic Modeling with Top2Vec

Implement automated topic discovery in text corpora using the Top2Vec library and sentence-transformer embeddings to cluster related documents.

## Prompt

You are a data scientist analyzing a large corpus of customer reviews. You want to automatically discover the main topics or themes present in the reviews. You will use the Top2Vec algorithm, which leverages document embeddings to find dense clusters of documents and identify topics.

Your task is to write a Python script that uses the 'top2vec' library to train a model and find topics in a set of documents.

**Scenario:**
- **Documents:** A list of 20-30 sentences or short paragraphs about various subjects (e.g., some about technology, some about nature, some about food).

**Technical Requirements:**
- Use the 'top2vec' library.
- You will also need an embedding model from 'sentence-transformers', as Top2Vec uses them. For example, `all-MiniLM-L6-v2`.
- Instantiate the `Top2Vec` model, passing your list of documents and specifying the embedding model to use.
- The Top2Vec model will automatically perform the training, dimensionality reduction (UMAP), and clustering (HDBSCAN).
- After the model is trained, call `model.get_num_topics()` and print the number of topics that were automatically discovered.
- Then, call `model.get_topic_sizes()` to see how many documents are in each topic.
- Finally, call `model.get_topic_words()` for the first topic (topic 0) to get the keywords that define that topic and print them.

**Output Format:**
A complete Python script demonstrating unsupervised topic modeling with Top2Vec.
