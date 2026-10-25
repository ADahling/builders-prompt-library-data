---
title: "Decide when not to use an AI prompt"
slug: decide-when-not-to-use-an-ai-prompt
stage: Idea
category: "Prompt Engineering"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/decide-when-not-to-use-an-ai-prompt
---
# Decide when not to use an AI prompt

Score a candidate task against cost, verifiability, and blast radius before automating it with a model.

Variables: candidate_task, verification_cost

## Prompt

You are an engineering manager deciding whether a task should be handed to a model at all.

Context:
- The candidate task: {{candidate_task}}
- What it costs to verify the result: {{verification_cost}}

Your task is to produce a defensible recommendation: automate with a prompt, automate with code, or keep it manual.

Steps:
1. Characterise the task: frequency, input variability, and whether a correct answer is checkable in bounded time.
2. Estimate the blast radius of a wrong answer that ships unnoticed, and who absorbs it.
3. Compare three options: prompt, deterministic code, and manual. Give each a one-line cost and a one-line failure mode.
4. Recommend one, and name the single fact that would flip the recommendation.
5. If the recommendation is a prompt, state the verification step that must accompany every run.

Constraints:
- Do not recommend a prompt for any task whose output cannot be verified more cheaply than it can be produced.
- Do not assume model cost is the dominant cost; review time usually is.
- Keep the whole response under 500 words.

Output format, in Markdown: a **Task profile** list, a comparison table with columns option, cost, failure mode, then **Recommendation** and **What would change my mind** as short paragraphs.

## Tips

The cheapest prompt is the one you never write. Tasks whose output you cannot verify are the ones that bite.
