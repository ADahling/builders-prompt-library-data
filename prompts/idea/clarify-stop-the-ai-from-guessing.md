---
title: "CLARIFY \u2014 Stop the AI from Guessing"
slug: clarify-stop-the-ai-from-guessing
stage: Idea
category: "Prompt Engineering"
grade: B
score: 70
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/clarify-stop-the-ai-from-guessing
---
# CLARIFY — Stop the AI from Guessing

Get three feature questions on data, user flow, and edge cases before coding, plus follow-up questions when answers lack detail.

## Prompt

Before writing any code, ask me 3 clarifying questions:

1. DATA STRUCTURE: What data does this feature need? What are the relationships? What fields are required vs optional?
2. USER FLOW: Walk me through the exact user journey step by step. What does the user see, click, and expect at each point?
3. EDGE CASES: What happens when data is empty, the user is not logged in, the network fails, or the input is invalid?

Do NOT generate any code until I've answered all three questions. If my answers are vague, ask follow-up questions until you have enough specificity to build correctly the first time.

## Tips

From Reddit r/lovable — tested across 500+ prompts. Prevents the AI from making assumptions that lead to rewrites. Source: reddit.com/r/lovable/comments/1px6vpg
