---
title: "Identify and Remove Dead Code"
slug: identify-and-remove-dead-code
stage: Test
category: "Cleanup & Warnings"
grade: B
score: 77
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/identify-and-remove-dead-code
---
# Identify and Remove Dead Code

Review supplied code for unused or unreachable segments and get a list of dead code with reasoning for each recommended removal.

Variables: code_snippet

## Prompt

Please analyze the provided code and identify any segments that can be classified as dead code, i.e., code that is never executed or used. Here is the code: {{code_snippet}}. Compile a list of the dead code segments along with reasoning for their removal.

## Tips

Use this prompt to help identify potentially unused or unnecessary code in your project.
