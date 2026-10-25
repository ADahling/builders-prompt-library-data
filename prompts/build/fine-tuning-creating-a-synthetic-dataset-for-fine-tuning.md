---
title: "Fine-Tuning: Creating a Synthetic Dataset for Fine-Tuning"
slug: fine-tuning-creating-a-synthetic-dataset-for-fine-tuning
stage: Build
category: "LLM & AI Integration"
grade: A
score: 87
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/fine-tuning-creating-a-synthetic-dataset-for-fine-tuning
---
# Fine-Tuning: Creating a Synthetic Dataset for Fine-Tuning

Write a Python script using a teacher model to generate 10 fictional API question-answer pairs as JSONL training data for fine-tuning.

## Prompt

You need to fine-tune a model for a specific task, but you lack a large, high-quality dataset. You decide to use a powerful, expensive model (a 'teacher' model) to generate a synthetic dataset, which you will then use to fine-tune a smaller, more efficient 'student' model.

Your task is to write a Python script that uses a 'teacher' model (like GPT-5) to generate training data in the JSONL format required for fine-tuning.

**Scenario:**
- **Task:** Create a chatbot that answers questions about a fictional company's API documentation.
- **Goal:** Generate 10 high-quality question/answer pairs for the fine-tuning dataset.

**Technical Requirements:**
- Use the 'openai' Python library.
- **Step 1 (Define Context):** Create a system prompt for the teacher model that contains a small, fictional API documentation snippet. (e.g., "You are an expert on the 'PixelPush' API. The endpoint `POST /v1/images` creates a new image. It requires a `prompt` (string) and `width` (int). It returns an `image_url`.").
- **Step 2 (Generate Data):** Write a loop that runs 10 times. In each iteration:
    -   Make a call to GPT-5 with the system prompt.
    -   The user prompt should be: "Generate a single, unique user question about the PixelPush API and the ideal, concise answer for it. Format the output as a JSON object with keys 'question' and 'answer'."
    -   Use JSON mode to ensure the output is valid JSON.
- **Step 3 (Format for Fine-Tuning):** Take the generated 'question' and 'answer' and format them into the OpenAI fine-tuning structure: `{"messages": [{"role": "user", "content": question}, {"role": "assistant", "content": answer}]}`.
- **Step 4 (Save to File):** Append this JSONL string to a file named `synthetic_dataset.jsonl`.

**Output Format:**
A complete Python script that generates a `synthetic_dataset.jsonl` file with 10 training examples.
