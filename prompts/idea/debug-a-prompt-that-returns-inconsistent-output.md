---
title: "Debug a prompt that returns inconsistent output"
slug: debug-a-prompt-that-returns-inconsistent-output
stage: Idea
category: "Prompt Engineering"
grade: A+
score: 95
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/debug-a-prompt-that-returns-inconsistent-output
---
# Debug a prompt that returns inconsistent output

Diagnose why the same prompt gives different answers each run and fix the instability at its source.

Variables: prompt_text, observed_variance

## Prompt

You are a prompt engineer diagnosing an unstable prompt.

Context:
- The prompt under test: {{prompt_text}}
- What varies between runs: {{observed_variance}}

Your task is to find the instruction that permits the variance and remove the ambiguity.

Steps:
1. Read the prompt as an adversary. List every sentence that admits more than one reading.
2. For each, rank the likely contribution to the observed variance as high, medium, or low, with one line of reasoning.
3. Identify unpinned surfaces: missing output schema, unbounded length, unranked criteria, unspecified tie-breaks.
4. Rewrite the highest-contribution instructions so only one reading survives.
5. Propose a cheap regression check: three inputs whose correct outputs are known, so the team can rerun after any edit.

Constraints:
- Do not recommend lowering temperature as the primary fix; treat model settings as a last resort and say why.
- Keep the rewritten prompt within 20 percent of the original length.
- Flag anything that cannot be stabilised in the prompt and belongs in code instead.

Output format, in Markdown: a findings table with columns instruction, ambiguity, severity, fix, then the **Revised prompt** in a fenced code block, then a **Regression checks** list.

## Tips

Inconsistency is usually an unpinned format or a question with two defensible readings, not model randomness.
