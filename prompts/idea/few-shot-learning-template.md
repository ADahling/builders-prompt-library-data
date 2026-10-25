---
title: "Few-Shot Learning Template"
slug: few-shot-learning-template
stage: Idea
category: "Prompt Engineering"
grade: A
score: 86
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/few-shot-learning-template
---
# Few-Shot Learning Template

Get an explanation of the pattern in your input-output examples, followed by a new output that applies that pattern to a fresh input.

Variables: number_of_examples, example_1_input, example_1_output, example_2_input, example_2_output, example_3_input, example_3_output, new_input

## Prompt

I want you to learn a pattern from examples and apply it to new inputs.

Here are {{number_of_examples}} examples of the pattern:

Example 1:
Input: {{example_1_input}}
Output: {{example_1_output}}

Example 2:
Input: {{example_2_input}}
Output: {{example_2_output}}

Example 3:
Input: {{example_3_input}}
Output: {{example_3_output}}

Now apply the same pattern to this new input:
Input: {{new_input}}

Before generating the output, first describe the pattern you identified from the examples. Then apply it consistently to the new input.

## Tips

The gold standard for teaching AI new patterns without fine-tuning. Works best with 3-5 diverse examples.
