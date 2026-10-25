---
title: "Cost Optimization: Token Counting Before API Call"
slug: cost-optimization-token-counting-before-api-call
stage: Build
category: "LLM & AI Integration"
grade: A
score: 84
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/cost-optimization-token-counting-before-api-call
---
# Cost Optimization: Token Counting Before API Call

Generate a Python script using the tiktoken library to calculate token counts and estimate API request costs for the GPT-5 model.

## Prompt

As a developer managing an application with a high volume of LLM API calls, you need to control costs by preventing unexpectedly large and expensive requests. A key strategy is to estimate the number of tokens in a prompt *before* sending it to the API.

Your task is to write a Python script that uses the 'tiktoken' library, which is OpenAI's tokenizer, to count the tokens in a given text for a specific model.

**Scenario:**
- **Model:** 'gpt-5'
- **Text to Analyze:** A long piece of text. For this example, you can use a few paragraphs of lorem ipsum or any other placeholder text that is several hundred words long.
- **Cost Assumption:** Assume a cost of $5.00 per 1 million input tokens for the 'gpt-5' model.

**Technical Requirements:**
- Use the 'tiktoken' Python library.
- The script must get the correct encoding for the 'gpt-5' model using `tiktoken.encoding_for_model()`.
- It should then encode the input text to get a list of token integers.
- Count the number of tokens by getting the length of this list.
- Calculate the estimated cost of sending this text as a prompt to the API based on the assumed cost.
- The script must print the token count and the estimated cost to the console in a clear, human-readable format.

**Output Format:**
A complete, executable Python script that demonstrates pre-call token counting and cost estimation.
