---
title: "The Guardrail Prompt (Prevent Unwanted Changes)"
slug: the-guardrail-prompt-prevent-unwanted-changes
stage: Idea
category: "Prompt Engineering"
grade: B
score: 78
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/the-guardrail-prompt-prevent-unwanted-changes
---
# The Guardrail Prompt (Prevent Unwanted Changes)

Set up coding session rules that limit edits to requested changes, require scope clarification, and call for a change list after each update.

## Prompt

IMPORTANT RULES FOR THIS ENTIRE SESSION:

1. Only make the exact changes I request. Do not modify, remove, or alter any other code, styling, or page elements unless I explicitly ask you to.
2. If my request conflicts with existing code or functionality, PAUSE and ask for confirmation before proceeding.
3. Do not refactor, reorganize, rename, or "improve" anything I haven't asked you to touch.
4. Do not remove comments, console logs, or debugging code unless I specifically ask.
5. If you're unsure about scope, ask: "Should I also change X?" rather than assuming yes.
6. After making changes, list exactly what you changed and confirm nothing else was modified.
7. If you notice other issues while working, note them separately as "Observations" but do NOT fix them unless I ask.

Acknowledge these rules before we begin.

## Tips

From Ran the Builder and VibeCodex. Essential when working with AI on existing codebases. Prevents the AI from 'helping' by breaking things you didn't ask it to touch.
