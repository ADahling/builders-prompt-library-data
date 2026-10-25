---
title: "Cost Optimization: Batch Processing with OpenAI API"
slug: cost-optimization-batch-processing-with-openai-api
stage: Build
category: "LLM & AI Integration"
grade: A
score: 84
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/cost-optimization-batch-processing-with-openai-api
---
# Cost Optimization: Batch Processing with OpenAI API

Get a Python script that prepares JSONL review sentiment requests, uploads them to OpenAI's Batch API, and prints the batch ID and initial status.

## Prompt

You have a dataset of 10,000 product reviews that need sentiment analysis. Sending 10,000 synchronous API calls would take hours and hit rate limits. OpenAI offers a Batch API that processes requests asynchronously at a 50% discount.

Your task is to write a Python script that demonstrates how to create and submit a batch job using the OpenAI API.

**Scenario:**
- You need to create a JSONL file containing the requests.
- Submit the file to the Batch API.

**Technical Requirements:**
- Use the 'openai' Python library.
- **Step 1 (Prepare Data):** Create a string containing at least two valid JSONL lines formatted for the Batch API. Each line must have a `custom_id`, `method` ("POST"), `url` ("/v1/chat/completions"), and `body` (the standard chat completion payload).
- **Step 2 (Upload File):** Save this string to a local file `batch_requests.jsonl`. Then, use `client.files.create()` to upload this file to OpenAI, setting `purpose="batch"`.
- **Step 3 (Create Batch):** Use `client.batches.create()` to start the batch job. Pass the `file_id` from Step 2, set `endpoint="/v1/chat/completions"`, and `completion_window="24h"`.
- **Step 4 (Output):** Print the `batch_id` and the initial `status` of the batch job to the console. (You do not need to write the polling logic to wait for completion in this script).

**Output Format:**
A complete Python script demonstrating the setup and submission of an OpenAI Batch API job.
