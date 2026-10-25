---
title: "Develop a Chain-of-Thought Prompt for Debugging Code"
slug: develop-a-chain-of-thought-prompt-for-debugging-code
stage: Idea
category: "Prompt Engineering"
grade: B
score: 77
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/develop-a-chain-of-thought-prompt-for-debugging-code
---
# Develop a Chain-of-Thought Prompt for Debugging Code

Construct a structured debugging framework that guides an AI to identify errors and explain logical fixes through step-by-step reasoning.

Variables: language

## Prompt

You are a senior software engineer specializing in debugging complex code. Your task is to develop a chain-of-thought prompt that guides an AI assistant to debug a snippet of {{language}} code. The AI should not just provide the corrected code, but should explain its reasoning process step-by-step.

The prompt must instruct the AI to perform the following steps:

1.  **Analyze the Code**: First, understand the purpose of the code snippet and its expected behavior.
2.  **Identify the Error**: Second, identify the bug in the code. This could be a syntax error, a logical error, or a runtime error.
3.  **Explain the Error**: Third, explain why the bug is occurring. This explanation should be clear and easy for a junior developer to understand.
4.  **Propose a Solution**: Fourth, suggest a correction for the bug.
5.  **Provide Corrected Code**: Finally, provide the complete, corrected code snippet.

The prompt should be general enough to be used with any {{language}} code snippet. The user will provide the code snippet to be debugged.

## Tips

This prompt uses the chain-of-thought technique to guide an AI through the process of debugging code, making it a great learning tool for junior developers.
