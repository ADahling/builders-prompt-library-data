---
title: "API Integration: Using a Local LLM with Ollama\n"
slug: api-integration-using-a-local-llm-with-ollama
stage: Build
category: "LLM & AI Integration"
grade: A
score: 82
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/api-integration-using-a-local-llm-with-ollama
---
# API Integration: Using a Local LLM with Ollama


Implement a Python script using the 'requests' library to interact with a local Ollama REST API for private and cost-effective LLM inference.

## Prompt

You are developing an application that requires an LLM, but for privacy and cost reasons, you want to run the model locally on your own machine. You will use Ollama, a popular tool for running open-source LLMs locally.

Your task is to write a Python script that interacts with a locally running Ollama model via its REST API.

**Prerequisites (for the user):**
- Ollama is installed and running.
- A model has been pulled, e.g., by running `ollama pull llama3` in the terminal.

**Scenario:**
- **Model:** `llama3`
- **Prompt:** "Why is the sky blue? Explain it simply."

**Technical Requirements:**
- Use the 'requests' Python library.
- The Ollama API server runs by default at `http://localhost:11434`.
- You will make a POST request to the `/api/generate` endpoint.
- The request body should be a JSON object containing:
    - `model`: the name of the local model to use (e.g., "llama3").
    - `prompt`: the user's prompt.
    - `stream`: `False` (for a single, non-streaming response).
- The script should parse the JSON response from the API, extract the `response` field, and print it to the console.
- Include error handling in case the script cannot connect to the Ollama server.

**Output Format:**
A complete, executable Python script that demonstrates how to call a local Ollama model.
