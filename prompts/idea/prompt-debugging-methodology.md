---
title: "Prompt Debugging Methodology"
slug: prompt-debugging-methodology
stage: Idea
category: "Prompt Engineering"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/prompt-debugging-methodology
---
# Prompt Debugging Methodology

Analyze and optimize underperforming prompts by identifying logical flaws, ambiguity, and constraints to produce a revised, high-quality version.

Variables: my_prompt, expected_output, actual_output

## Prompt

You are a prompt debugging specialist. My prompt is not producing the expected output. Help me debug it.

My prompt:
{{my_prompt}}

Expected output:
{{expected_output}}

Actual output:
{{actual_output}}

Debug using this methodology:
1. **Clarity Check**: Is the instruction ambiguous? Could it be interpreted differently?
2. **Context Check**: Does the AI have enough context to produce the expected output?
3. **Constraint Check**: Are the constraints too strict, too loose, or contradictory?
4. **Format Check**: Is the expected output format clearly specified?
5. **Example Check**: Would adding examples (few-shot) help?
6. **Decomposition Check**: Should this be broken into multiple prompts?
7. **Model Check**: Is this task within the model's capabilities?
8. **Temperature Check**: Is the temperature/sampling appropriate for this task?

For each issue found:
- The problem
- Why it causes the wrong output
- The fix
- The revised prompt section

Provide the complete fixed prompt at the end.

## Tips

Prompt debugging is a skill. This systematic methodology finds the root cause faster than trial and error.
