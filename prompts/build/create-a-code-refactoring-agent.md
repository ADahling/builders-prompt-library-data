---
title: "Create a Code Refactoring Agent"
slug: create-a-code-refactoring-agent
stage: Build
category: "AI Agent Development"
grade: A+
score: 91
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-code-refactoring-agent
---
# Create a Code Refactoring Agent

Automate Python code optimization by identifying smells and generating refactored versions with structured JSON explanations.

Variables: python_function

## Prompt

You are an AI assistant that helps developers refactor their code. Your task is to create an agent that can take a Python function, analyze it, and suggest specific improvements.

**Agent's Task:**

Given a Python function, the agent should:
1.  Identify any code smells (e.g., long functions, duplicate code, unclear variable names).
2.  Suggest a refactored version of the code that is cleaner, more efficient, and more readable.
3.  Provide a clear explanation of the changes made and why they are beneficial.

**Implementation:**

*   This can be implemented as a single-prompt LLM call.
*   The prompt should be carefully engineered to guide the LLM.
*   **Prompt Structure:**
    *   **Role:** "You are an expert Python developer specializing in code quality and refactoring."
    *   **Task:** "Analyze the following Python function and provide a refactored version."
    *   **Output Format:** "Your output must be a JSON object with two keys: `refactored_code` and `explanation`. The explanation should be a bulleted list of the changes."
    *   **Input:** The user provides the `{{python_function}}` to be refactored.

**Example Input:**

*   A Python function that is overly complex or poorly written.

**Output:**

A Python script that defines a function to call the LLM with this structured prompt and then parses and prints the JSON response.
