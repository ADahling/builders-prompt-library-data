---
title: "Multimodal AI: Image Analysis with OpenAI GPT-4o"
slug: multimodal-ai-image-analysis-with-openai-gpt-4o
stage: Build
category: "LLM & AI Integration"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/multimodal-ai-image-analysis-with-openai-gpt-4o
---
# Multimodal AI: Image Analysis with OpenAI GPT-4o

Implement a Python script using the OpenAI API and GPT-5 to analyze a city street image and identify visible safety hazards.

## Prompt

You are a developer building an application that can 'see' and understand images. You want to use OpenAI's GPT-5 model to analyze an image and answer questions about it.

Your task is to write a Python script that sends an image and a text prompt to the OpenAI API.

**Scenario:**
- **Image:** A publicly accessible image of a busy city street. Use a placeholder URL for the image, for example: `https://example.com/path/to/city_street.jpg`. (In a real scenario, you would provide a valid URL or a base64-encoded image).
- **Question:** "What are three potential safety hazards visible in this image?"

**Technical Requirements:**
- Use the 'openai' Python library.
- Use the 'gpt-5' model, as it is designed for multimodal inputs.
- The `messages` payload sent to the API must be an array containing two dictionaries:
    1.  The first dictionary is for the text prompt, asking the question.
    2.  The second dictionary is for the image, specifying its type ('image_url') and the URL.
- The script should make the API call and print the model's text-based response, which should identify potential safety hazards in the described image.
- Handle your API key securely.

**Output Format:**
A complete, executable Python script demonstrating how to perform image analysis with GPT-5.
