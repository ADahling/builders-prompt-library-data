---
title: "Beginner: Your First API Call with Python and OpenAI"
slug: beginner-your-first-api-call-with-python-and-openai
stage: Build
category: "LLM & AI Integration"
grade: A
score: 84
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/beginner-your-first-api-call-with-python-and-openai
---
# Beginner: Your First API Call with Python and OpenAI

Create a commented, beginner-friendly Python script to perform an initial OpenAI API call using environment variables and error handling.

## Prompt

You are a new AI developer about to make your very first call to the OpenAI API. You need a simple, complete, and well-commented Python script that serves as a 'Hello, World!' for LLM integration.

Your task is to write a Python script that sends a basic prompt to the OpenAI API and prints the response.

**Scenario:**
- **Goal:** Ask the AI a simple question.
- **Question:** "What are the three primary colors?"

**Technical Requirements:**
- Use the 'openai' Python library.
- The script must be complete and runnable from top to bottom.
- **API Key Handling:** Show how to load the API key from an environment variable named `OPENAI_API_KEY`. Include a check to ensure the key is set and print an error message if it's not.
- **Client Initialization:** Show how to create the OpenAI client instance.
- **API Call:** Make a call to `client.chat.completions.create()`.
    -   Use a common, cost-effective model like `gpt-5`.
    -   The `messages` array should contain a single object with `role: 'user'` and `content: 'What are the three primary colors?'`.
- **Response Handling:**
    -   Extract the content from the first choice in the response.
    -   Print the AI's answer to the console.
- **Comments:** The script must be heavily commented, explaining what each line does for a beginner.

**Output Format:**
A single, executable Python script that is easy for a beginner to understand and run.
