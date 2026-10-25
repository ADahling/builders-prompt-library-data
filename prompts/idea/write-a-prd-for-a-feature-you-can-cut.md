---
title: "Write a PRD for a feature you can cut"
slug: write-a-prd-for-a-feature-you-can-cut
stage: Idea
category: "Idea to PRD"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-a-prd-for-a-feature-you-can-cut
---
# Write a PRD for a feature you can cut

Specify a feature in slices with an explicit cut line, so scope can be reduced without a rewrite.

Variables: feature_idea, deadline_context

## Prompt

You are a product engineer writing a requirements document for a feature with a fixed deadline.

Context:
- The idea: {{feature_idea}}
- The deadline and what is driving it: {{deadline_context}}

Your task is to specify the feature so scope can be cut under pressure without redesigning it.

Steps:
1. State the problem and the user it affects, with the evidence you have. Mark anything you are assuming.
2. Define the success metric and the current baseline. If there is no baseline, say how it will be measured before launch.
3. Break the feature into slices ordered by value delivered, each independently shippable and testable.
4. Draw the cut line: which slices constitute launch, and which are explicitly deferred. State what the launch version does not do.
5. Write the acceptance criteria per launch slice as observable behaviours, including the empty, loading, and error states.
6. List the open questions with an owner and a date by which each must be answered.

Constraints:
- Do not describe implementation or choose a technology.
- Every requirement must be testable by someone who did not write it.
- Do not leave a slice partly above and partly below the cut line.

Output format, in Markdown with these sections in order: Problem, Evidence and assumptions, Success metric, Slices (a table with columns slice, value, in launch), Cut line, Acceptance criteria per slice, Open questions with owner and date.

## Tips

Draw the cut line in the document before the deadline forces someone to draw it in a hurry.
