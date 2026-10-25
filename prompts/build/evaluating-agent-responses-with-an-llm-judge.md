---
title: "Evaluating Agent Responses with an LLM Judge"
slug: evaluating-agent-responses-with-an-llm-judge
stage: Build
category: "AI Agent Development"
grade: A+
score: 91
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/evaluating-agent-responses-with-an-llm-judge
---
# Evaluating Agent Responses with an LLM Judge

Build a Python LLM judge that scores agent responses for helpfulness, clarity, and harmlessness, with JSON scores and justifications.

Variables: prompt, response, evaluation_criteria

## Prompt

Develop a system for evaluating the quality of an AI agent's responses using another LLM as a "judge". This is a common and scalable technique for agent evaluation.

**Your Task:**

Create a Python script that defines an "LLM Judge" that rates an agent's response based on a given set of criteria.

**Evaluation Workflow:**

1.  **Inputs for the Judge:** The judge will receive:
    *   The original user `{{prompt}}`.
    *   The agent's `{{response}}`.
    *   A set of `{{evaluation_criteria}}`.
2.  **The Judge's Prompt:**
    *   You will need to craft a detailed prompt for the judge LLM.
    *   This prompt should instruct the judge to act as an impartial evaluator.
    *   It should ask the judge to provide a score (e.g., 1-10) for each of the evaluation criteria.
    *   It should also ask for a brief written justification for the scores.
    *   The output should be in a structured format, like JSON, for easy parsing.
3.  **Evaluation Criteria:**
    *   For this task, use the following criteria:
        *   **Helpfulness:** How well does the response answer the user's prompt?
        *   **Clarity:** Is the response easy to understand?
        *   **Harmlessness:** Is the response free of any unsafe or inappropriate content?
4.  **Execution:**
    *   Your script should take a sample prompt and response.
    *   It will then call the judge LLM with the crafted prompt.
    *   Finally, it will parse the judge's JSON output and print the evaluation results.

**Output:**

A Python script that implements the LLM Judge. The script should include the judge's prompt and an example of it evaluating a sample agent response. The final output should be the parsed JSON evaluation.
