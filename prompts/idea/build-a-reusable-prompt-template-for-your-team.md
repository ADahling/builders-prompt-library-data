---
title: "Build a reusable prompt template for your team"
slug: build-a-reusable-prompt-template-for-your-team
stage: Idea
category: "Prompt Engineering"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/build-a-reusable-prompt-template-for-your-team
---
# Build a reusable prompt template for your team

Turn a prompt that worked once into a parameterised template the whole team can run.

Variables: working_prompt, team_context

## Prompt

You are a staff engineer who maintains your team's shared prompt library.

Context:
- A prompt that worked in one session: {{working_prompt}}
- The team and codebase it must generalise to: {{team_context}}

Your task is to convert the one-off prompt into a template other people can run without asking the author anything.

Steps:
1. Separate the durable instruction from the session-specific detail. The durable part stays; the detail becomes a variable.
2. Name each variable in snake_case and write a one-line description and an example value for each.
3. Add the guardrails a stranger needs: what the model must not assume, and what it should do when a variable is left blank.
4. Add a short usage note covering when to reach for this template and when not to.
5. State the acceptance criteria: what a good run of this template produces, so a reviewer can tell a pass from a fail.

Constraints:
- No more than six variables. If you need more, the template is doing two jobs; split it and say so.
- Do not change what the original prompt achieved.
- Avoid model-specific syntax so the template survives a model swap.

Output format, in Markdown: a **Template** section holding the prompt in a fenced code block, a **Variables** table with columns name, description, example, then **When to use**, **When not to use**, and **Acceptance criteria** as bulleted lists.

## Tips

The test of a template is whether a teammate can run it without asking you a question first.
