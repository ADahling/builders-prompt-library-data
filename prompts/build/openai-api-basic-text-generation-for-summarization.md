---
title: "OpenAI API: Basic Text Generation for Summarization"
slug: openai-api-basic-text-generation-for-summarization
stage: Build
category: "LLM & AI Integration"
grade: A+
score: 90
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/openai-api-basic-text-generation-for-summarization
---
# OpenAI API: Basic Text Generation for Summarization

Create a Python script that reads a text file and uses the OpenAI API to generate a multi-paragraph abstractive summary with error handling.

## Prompt

Act as a backend developer integrating the OpenAI API for a text summarization service.

Your task is to generate a Python script that takes a long article as input and uses the OpenAI Completions API (with a model like "GPT-5" or a newer chat-based model) to generate a concise summary.

**Constraints & Requirements:**
- The script must read the article content from a file named 'article.txt'.
- Use the 'openai' Python library.
- Your script should include comments explaining each part of the process: reading the file, setting up the API call, making the request, and printing the summary.
- The summary should be no more than 3 paragraphs.
- The prompt sent to the OpenAI API must be carefully crafted to request a high-quality, abstractive summary, not just a simple extraction of sentences.
- Include error handling for potential API errors or file not found issues.
- Use environment variables to manage the OpenAI API key for security.

**Output Format:**
Provide a single Python code block. The script should be ready to run, assuming the 'openai' library is installed and the API key is set as an environment variable 'OPENAI_API_KEY'.

**Example Input Article ('article.txt'):**
(A long article about the history of artificial intelligence...)

**Desired Output (Printed to console):**
A well-written, 3-paragraph summary of the provided article.
