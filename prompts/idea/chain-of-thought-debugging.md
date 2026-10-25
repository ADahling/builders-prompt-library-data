---
title: "Chain of Thought Debugging"
slug: chain-of-thought-debugging
stage: Idea
category: "Prompt Engineering"
grade: A
score: 83
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/chain-of-thought-debugging
---
# Chain of Thought Debugging

Get a bug diagnosis with possible causes, evidence checks, a minimal proposed fix, its risks, and a verification test before jumping to code.

## Prompt

I have a bug: [describe the bug, what you expected, what actually happened].

Before suggesting a fix, think step by step:
1. What are the possible root causes? List at least 3.
2. For each cause, what evidence would confirm or rule it out?
3. What is the most likely cause and why?
4. Propose a minimal fix that addresses only the root cause.
5. Explain what could go wrong with your fix.
6. Suggest a test to verify the fix works.

Do NOT jump to code. Walk me through your reasoning first.

## Tips

Forces AI to reason before coding. Dramatically better debugging results.
