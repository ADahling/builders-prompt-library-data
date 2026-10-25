---
title: "Multimodal AI: Document Parsing with OpenAI Vision"
slug: multimodal-ai-document-parsing-with-openai-vision
stage: Build
category: "LLM & AI Integration"
grade: A
score: 88
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/multimodal-ai-document-parsing-with-openai-vision
---
# Multimodal AI: Document Parsing with OpenAI Vision

Generate a Python script that uses GPT-5's vision capabilities to extract structured invoice data from local images into JSON format.

## Prompt

You are automating a data entry process. You have scanned images of invoices and need to extract structured data (Invoice Number, Total Amount, Date) from them. You will use OpenAI's GPT-5 vision capabilities.

Your task is to write a Python script that takes an image of an invoice and extracts the data into a JSON format.

**Scenario:**
- **Image:** Assume you have a local file named `invoice_sample.jpg`.
- **Goal:** Extract `invoice_number`, `date`, and `total_amount`.

**Technical Requirements:**
- Use the 'openai' Python library.
- Read the local image file and encode it in base64.
- Construct the `messages` payload with the text prompt and the base64 image URL.
- The text prompt must explicitly ask the model to act as a data extraction tool and return *only* a JSON object with the keys `invoice_number`, `date`, and `total_amount`.
- Use the `response_format={"type": "json_object"}` parameter to ensure the output is valid JSON.
- Parse the resulting JSON string and print the Python dictionary.

**Output Format:**
A complete Python script. Include a comment that the user needs an `invoice_sample.jpg` file in the same directory.
