---
title: "The Universal Prompt Starter (Context + Task + Constraints)"
slug: the-universal-prompt-starter-context-task-constraints
stage: Idea
category: "Prompt Engineering"
grade: A+
score: 94
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/the-universal-prompt-starter-context-task-constraints
---
# The Universal Prompt Starter (Context + Task + Constraints)

Get a task recap, clarifying questions, assumptions, and a step-by-step plan before work begins on a request with supplied context and constraints.

## Prompt

I want to [TASK] so that [SUCCESS CRITERIA].

First, read these files completely before responding:
[list any uploaded files, docs, or context]

DO NOT start executing yet. Instead:
1. Tell me what you understand about the task.
2. Ask me clarifying questions so we can refine the approach together.
3. List any assumptions you're making.
4. Propose a plan of attack with steps.
5. Only begin work once we've aligned.

Constraints:
- [Any specific requirements: tech stack, tone, length, format]
- [Any things to avoid: don't change X, don't use Y]
- [Success looks like: specific measurable outcome]

## Tips

Based on Ruben Hassid's 2026 workflow. This replaces complicated mega-prompts. Context + conversation beats instructions alone.
