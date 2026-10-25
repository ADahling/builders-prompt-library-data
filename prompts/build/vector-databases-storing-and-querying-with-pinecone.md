---
title: "Vector Databases: Storing and Querying with Pinecone"
slug: vector-databases-storing-and-querying-with-pinecone
stage: Build
category: "LLM & AI Integration"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/vector-databases-storing-and-querying-with-pinecone
---
# Vector Databases: Storing and Querying with Pinecone

Develop a Python script using the Pinecone API to implement an end-to-end vector database workflow for semantic product search.

## Prompt

As a senior AI engineer, you are building a scalable, enterprise-grade semantic search application. You have chosen Pinecone as your managed vector database.

Your task is to write a Python script that demonstrates the fundamental workflow of using the Pinecone API: creating an index, upserting vectors, and querying the index.

**Scenario:**
- **Index Name:** 'product-search'
- **Vector Dimension:** 8 (for this simplified example)
- **Vectors to Upsert:**
    - id="product-1", values=[0.1, 0.1, 0.1, 0.1, 0.1, 0.1, 0.1, 0.1], metadata={'name': 'Blender'}
    - id="product-2", values=[0.9, 0.9, 0.9, 0.9, 0.9, 0.9, 0.9, 0.9], metadata={'name': 'Toaster'}
- **Query Vector:** [0.8, 0.8, 0.8, 0.8, 0.8, 0.8, 0.8, 0.8]

**Technical Requirements:**
- Use the 'pinecone-client' Python library.
- Securely initialize Pinecone using API keys from environment variables ('PINECONE_API_KEY').
- Check if the 'product-search' index already exists. If not, create it with the correct dimension. Use a serverless spec for this example.
- Connect to the index.
- Upsert the two product vectors with their IDs and metadata.
- Perform a query using the query vector, asking for the top 1 result.
- The script should print the query response, which includes the ID and metadata of the most similar product ('Toaster').
- Include a final step to delete the index to clean up resources.

**Output Format:**
A complete, runnable Python script that covers the Pinecone workflow.
