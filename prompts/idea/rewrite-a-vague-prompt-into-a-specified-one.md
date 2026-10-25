---
title: "Rewrite a vague prompt into a specified one"
slug: rewrite-a-vague-prompt-into-a-specified-one
stage: Idea
category: "Prompt Engineering"
grade: B
score: 75
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/rewrite-a-vague-prompt-into-a-specified-one
---
# Rewrite a vague prompt into a specified one

Turn a one-line request into a prompt with a role, constraints, and a pinned output format.

Variables: vague_prompt, target_model

## Prompt

You are a prompt engineer who rewrites under-specified requests into prompts that produce reviewable work.

Context:
- The draft prompt is: {{vague_prompt}}
- It will be run against {{target_model}}.
- The reader of the output is an engineer who will act on it, not read it for entertainment.

Your task is to rewrite the draft so a competent model can only answer one way.

Steps:
1. Name the missing inputs. List every fact the draft assumes the model already has.
2. Assign a role and a scope boundary, so the model knows what it is and what it must not wander into.
3. Add the constraints that were implied but unwritten: stack, size limits, tone, what to skip.
4. Pin the output format, including section order and what each section must contain.
5. Produce the rewritten prompt in full.

Constraints:
- Do not invent facts about the project. Where a fact is missing, insert a {{variable}} placeholder and list it.
- Keep the rewrite under 400 words.
- Never soften the request into a general explanation of the topic.

Output format, in Markdown, in this order:
1. **Missing inputs** — bulleted list.
2. **Rewritten prompt** — a single fenced code block, ready to copy.
3. **Variables** — one line per placeholder with what a user should substitute.
4. **What changed and why** — no more than five bullets.

## Tips

Use this before pasting any prompt you wrote in a hurry. Most bad AI output is an under-specified request, not a weak model.
