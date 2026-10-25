---
title: "Perplexity API: Grounded Web Search and Summarization"
slug: perplexity-api-grounded-web-search-and-summarization
stage: Build
category: "LLM & AI Integration"
grade: A+
score: 94
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/perplexity-api-grounded-web-search-and-summarization
---
# Perplexity API: Grounded Web Search and Summarization

Build a Python script that integrates the Perplexity API to perform real-time web research and generate summarized answers with citations.

## Prompt

As a research assistant bot developer, you want to provide users with up-to-date answers backed by real-time web search. You have chosen the Perplexity API (Sonar models) for this task.

Your task is to write a Python script that queries the Perplexity API to research a recent event and provide a summarized answer with citations.

**Scenario:**
- **Query:** "What are the latest developments in solid-state battery technology as of 2024?"

**Technical Requirements:**
- Use the 'requests' library or the OpenAI Python SDK (since Perplexity's API is OpenAI-compatible).
- Set the base URL to `https://api.perplexity.ai/chat/completions`.
- Use the `sonar-pro` or `sonar-reasoning-pro` model.
- Authenticate using the `SONAR_API_KEY` environment variable as a Bearer token.
- Send the user's query in the `messages` array.
- The script should print the model's response, which should naturally include inline citations (e.g., [1], [2]) based on its web search.
- Ensure you handle potential API errors gracefully.

**Output Format:**
A complete, executable Python script that demonstrates how to use the Perplexity API for grounded research.
