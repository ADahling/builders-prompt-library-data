---
title: "What is a Logic Bomb?"
slug: what-is-a-logic-bomb
stage: Secure
category: "Security Checklist"
grade: A
score: 82
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/what-is-a-logic-bomb
---
# What is a Logic Bomb?

Identify and neutralize logic bombs in critical codebases by recognizing malicious triggers, red flags, and safe analysis procedures.

Variables: code_type

## Prompt

You are a software developer who has been asked to review a colleague's code for any potential security issues. You are concerned about the possibility of a logic bomb, a piece of malicious code that is triggered by a specific condition. Your task is to review the code and to look for any signs of a logic bomb.

Context:
- The code is a `{{code_type}}` that is part of a critical business application.
- The colleague who wrote the code is leaving the company on bad terms.

Provide:
1. An explanation of what a logic bomb is and some examples of trigger conditions (e.g., a specific date, the absence of a specific user account).
2. A list of red flags to look for in the code that might indicate the presence of a logic bomb (e.g., obfuscated code, unusual date/time checks, code that is not related to the application's functionality).
3. A plan for how to safely analyze the suspicious code without triggering the logic bomb.

## Tips

A prompt that deals with an interesting and potentially very damaging type of insider threat.
