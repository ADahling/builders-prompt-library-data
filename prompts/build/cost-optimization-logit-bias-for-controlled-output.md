---
title: "Cost Optimization: Logit Bias for Controlled Output"
slug: cost-optimization-logit-bias-for-controlled-output
stage: Build
category: "LLM & AI Integration"
grade: A
score: 84
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/cost-optimization-logit-bias-for-controlled-output
---
# Cost Optimization: Logit Bias for Controlled Output

Implement a Python script using OpenAI's logit_bias and tiktoken to restrict LLM output to specific tokens for efficient classification.

## Prompt

You are building a classification system using an LLM. You want the model to respond with only one of a few predefined class names (e.g., "Sales", "Support", "Billing") and nothing else. Using `logit_bias` can force the model to only use specific tokens, which is more reliable and cheaper than text-based prompting.

Your task is to write a Python script that uses the `logit_bias` parameter in the OpenAI API to restrict the model's output to a specific set of words.

**Scenario:**
- **Allowed Words:** "Red", "Green", "Blue"
- **Prompt:** "What is your favorite color?"

**Technical Requirements:**
- Use the 'openai' and 'tiktoken' libraries.
- **Step 1 (Get Token IDs):** You first need to find the integer token IDs for your allowed words. Use the `tiktoken` library to tokenize "Red", "Green", and "Blue". Be aware that a word can be multiple tokens (e.g., with a leading space). You must get the correct token IDs.
- **Step 2 (Construct Logit Bias):** Create a dictionary for the `logit_bias` parameter. The keys should be the string representations of the token IDs, and the value for each should be 100 (a high value to make them highly likely).
- **Step 3 (Make API Call):** Make a call to the OpenAI Chat Completions API (e.g., with `gpt-5`).
    -   Pass the prompt.
    -   Pass the `logit_bias` dictionary you created.
    -   Set `max_tokens` to 1 to ensure only one token is generated.
- **Step 4 (Print Result):** Print the model's response. It should be one of "Red", "Green", or "Blue".

**Output Format:**
A complete Python script demonstrating the use of `logit_bias`.
