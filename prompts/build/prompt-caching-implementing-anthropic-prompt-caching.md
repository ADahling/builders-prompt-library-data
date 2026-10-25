---
title: "Prompt Caching: Implementing Anthropic Prompt Caching"
slug: prompt-caching-implementing-anthropic-prompt-caching
stage: Build
category: "LLM & AI Integration"
grade: A+
score: 94
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/prompt-caching-implementing-anthropic-prompt-caching
---
# Prompt Caching: Implementing Anthropic Prompt Caching

Implement Anthropic prompt caching in Python to reduce latency and costs when performing multi-turn analysis on large documents.

## Prompt

You are building a document analysis tool using Anthropic's Claude Sonnet 5. Users frequently ask multiple questions about the same large document (e.g., a 100-page PDF). To reduce latency and costs, you need to implement Anthropic's Prompt Caching feature.

Your task is to write a Python script that demonstrates how to use prompt caching with the Anthropic API.

**Scenario:**
- **System Prompt:** A large block of text representing the document content (e.g., "Here is the full text of the annual report: ... [insert long text] ...").
- **User Queries:**
    1. "What was the total revenue for Q3?"
    2. "Who is the new CEO?"

**Technical Requirements:**
- Use the 'anthropic' Python SDK.
- Use the 'claude-sonnet-5-2026' model (or a newer version that supports caching).
- In the API call, structure the `system` parameter as a list of content blocks.
- To enable caching for the large document, add the `cache_control={"type": "ephemeral"}` parameter to the specific content block containing the document text.
- Make the first API call with the first user query. This will cache the system prompt.
- Make the second API call with the second user query. This call should benefit from the cache.
- Print the `usage` statistics from the response object for both calls. The second call should show a high number of `cache_read_input_tokens` and a low number of `input_tokens`, proving the cache worked.

**Output Format:**
A complete Python script demonstrating Anthropic prompt caching and printing the usage metrics.
