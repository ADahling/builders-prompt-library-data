---
title: "Adversarial Prompt Testing"
slug: adversarial-prompt-testing
stage: Idea
category: "Prompt Engineering"
grade: A+
score: 96
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/adversarial-prompt-testing
---
# Adversarial Prompt Testing

Identify and resolve prompt vulnerabilities like injections, biases, and hallucinations by stress-testing system instructions with specific attack vectors.

Variables: application_type, my_prompt

## Prompt

You are a prompt security researcher. I have written the following prompt for my {{application_type}}:

---
{{my_prompt}}
---

Your task is to stress-test this prompt for vulnerabilities:

1. **Injection Attacks**: Can a user input override the system instructions? Try 5 different injection techniques.
2. **Edge Cases**: What happens with empty input, extremely long input, special characters, or multiple languages?
3. **Hallucination Triggers**: What inputs might cause the model to confidently state false information?
4. **Bias Detection**: Does the prompt inadvertently favor certain demographics, viewpoints, or outcomes?
5. **Output Manipulation**: Can a user trick the prompt into producing harmful, off-topic, or unformatted output?

For each vulnerability found, provide:
- The attack vector (exact input that breaks it)
- The undesired output
- A specific fix to the prompt
- A hardened version of the relevant section

## Tips

Run this before deploying any user-facing prompt. Catches issues that manual review misses.
