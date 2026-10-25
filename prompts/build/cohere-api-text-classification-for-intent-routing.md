---
title: "Cohere API: Text Classification for Intent Routing"
slug: cohere-api-text-classification-for-intent-routing
stage: Build
category: "LLM & AI Integration"
grade: A
score: 86
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/cohere-api-text-classification-for-intent-routing
---
# Cohere API: Text Classification for Intent Routing

Implement a Python script using the Cohere Classify API to route customer support inquiries into categories like Billing or Sales.

## Prompt

As a developer building a customer support routing system, you need to classify incoming user messages into specific categories (intents) so they can be routed to the correct department (e.g., Billing, Technical Support, Sales).

Your task is to write a Python script that uses the Cohere Classify API to categorize a user message based on a set of examples.

**Scenario:**
- **Examples (Training Data):**
    - "I need a refund for my last purchase." -> "Billing"
    - "My credit card was charged twice." -> "Billing"
    - "The app keeps crashing when I open it." -> "Technical Support"
    - "How do I reset my password?" -> "Technical Support"
    - "I want to upgrade to the enterprise plan." -> "Sales"
    - "What are your pricing tiers?" -> "Sales"
- **Input to Classify:** "I can't log in to my account, it says invalid credentials."

**Technical Requirements:**
- Use the 'cohere' Python SDK.
- Authenticate using the `COHERE_API_KEY` environment variable.
- Prepare the examples as a list of `ClassifyExample` objects (or dictionaries, depending on the SDK version).
- Call the `co.classify()` method.
- Pass the input text and the examples.
- Use a suitable model like `embed-english-v3.0` (Cohere's classify endpoint uses embeddings under the hood).
- The script should print the predicted class (which should be "Technical Support") and the confidence score.

**Output Format:**
A complete Python script demonstrating few-shot text classification with the Cohere API.
