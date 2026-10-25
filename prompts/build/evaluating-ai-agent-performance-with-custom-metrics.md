---
title: "Evaluating AI Agent Performance with Custom Metrics"
slug: evaluating-ai-agent-performance-with-custom-metrics
stage: Build
category: "AI Agent Development"
grade: B
score: 77
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/evaluating-ai-agent-performance-with-custom-metrics
---
# Evaluating AI Agent Performance with Custom Metrics

Design and implement a Python-based evaluation framework to measure a technical support agent's performance using custom behavioral metrics.

## Prompt

You are an AI quality assurance engineer. Your task is to design a framework for evaluating the performance of a customer service AI agent. The evaluation must go beyond simple accuracy and include custom metrics that measure the quality of the agent's interaction.

**Agent to Evaluate:**

A conversational agent designed to help users troubleshoot technical issues with a software product.

**Evaluation Metrics:**

Define and implement the following custom metrics:

1.  **Resolution Rate:** The percentage of conversations where the user's issue was successfully resolved. This requires a way to determine resolution, perhaps by asking the user at the end of the conversation or by analyzing the conversation for keywords indicating success.
2.  **Steps to Resolution:** The average number of turns (user-agent exchanges) it takes to resolve an issue. A lower number is better.
3.  **Politeness Score:** A score from 1 to 5 that measures the agent's politeness. This can be assessed by a separate LLM-based judge, which is given the conversation and asked to rate the agent's tone.
4.  **Tool Use Efficiency:** If the agent uses tools, measure how effectively it uses them. For example, did it call the right tool with the right arguments on the first try?

**Evaluation Process:**

1.  **Dataset:** Create a small dataset of 20-30 sample conversations with predefined user problems.
2.  **Execution:** Run the agent on each conversation in the dataset and log the full interaction.
3.  **Analysis:** Write a Python script that takes the conversation logs and calculates the four metrics defined above.
4.  **Report:** The script should generate a report in JSON format summarizing the agent's performance.

**Input:**

*   A log file containing multiple conversations in a structured format (e.g., a list of JSON objects, each representing a conversation).

**Output:**

A JSON report with the calculated performance metrics.
