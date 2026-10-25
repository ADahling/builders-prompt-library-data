---
title: "Write evaluation criteria for an AI-generated answer"
slug: write-evaluation-criteria-for-an-ai-generated-answer
stage: Idea
category: "Prompt Engineering"
grade: A
score: 80
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-evaluation-criteria-for-an-ai-generated-answer
---
# Write evaluation criteria for an AI-generated answer

Define pass/fail criteria so a teammate can judge AI output without re-litigating the request.

Variables: task_description, quality_bar

## Prompt

You are a quality lead defining how AI output on a recurring task gets accepted or rejected.

Context:
- The task the model performs: {{task_description}}
- The bar the output must clear: {{quality_bar}}

Your task is to produce an evaluation rubric a reviewer can apply in under five minutes with no debate.

Steps:
1. Decompose the task into no more than five scored dimensions. Each must be observable in the output itself.
2. For each dimension, write the pass condition and the fail condition in concrete terms. No adjectives that two reviewers could read differently.
3. Assign weights that sum to 100 and justify each weight in one line.
4. Define the hard gates: conditions that fail the whole output regardless of score.
5. Provide one worked example of a pass and one of a fail, each with the score by dimension.

Constraints:
- Every criterion must be checkable from the output alone, without rerunning the model.
- Do not include criteria about tone unless the quality bar names tone.
- State explicitly what the rubric does not cover, so nobody assumes false coverage.

Output format, in Markdown: a rubric table with columns dimension, weight, pass condition, fail condition; a **Hard gates** list; then **Worked examples** with the per-dimension scores shown.

## Tips

Write the criteria before the prompt. If you cannot state what a pass looks like, the prompt is not ready.
