---
title: "Building a Self-Hosted Open-Source Agent"
slug: building-a-self-hosted-open-source-agent
stage: Build
category: "AI Agent Development"
grade: A
score: 82
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/building-a-self-hosted-open-source-agent
---
# Building a Self-Hosted Open-Source Agent

Get a Markdown guide with commands and code for running a local model through Ollama and connecting it to a LangChain agent with a basic tool.

## Prompt

Provide a guide on how to build and run an AI agent using entirely open-source models and frameworks, without relying on proprietary APIs like OpenAI.

**The Stack:**

1.  **LLM:** An open-source model like Llama 4 or Mistral. You will run this locally.
2.  **LLM Serving:** Use a tool like Ollama or vLLM to serve the model and provide an API endpoint.
3.  **Agent Framework:** LangChain or a similar framework.

**Guide Steps:**

1.  **Setting up the LLM:**
    *   Explain how to install Ollama.
    *   Show the command to download and run a specific model: `ollama run llama4`.
    *   Explain that Ollama provides an OpenAI-compatible API endpoint (usually at `http://localhost:11434/v1`).
2.  **Connecting LangChain to the Local LLM:**
    *   Show how to instantiate a `ChatOpenAI` object in LangChain but point it to the local Ollama endpoint by setting the `base_url` and `api_key` (the key can be any string for Ollama).
3.  **Building the Agent:**
    *   Create a simple ReAct agent with a basic tool (like a calculator).
    *   The process is the same as building an agent with GPT-5, but the underlying LLM is running on the user's machine.
4.  **Running the Agent:**
    *   Show how to run the agent and that it works completely offline (internet is only needed for tools).

**Output Format:**

A Markdown guide with code snippets and shell commands, walking a user through the entire process of setting up and running a fully self-hosted agent.
