---
title: "Generate a JSON structure for maintaining a code review checklist"
slug: generate-a-json-structure-for-maintaining-a-code-review-checklist
stage: Test
category: "Code Review"
grade: A
score: 80
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-a-json-structure-for-maintaining-a-code-review-checklist
---
# Generate a JSON structure for maintaining a code review checklist

Get a JSON checklist for your project's code reviews, with each review item mapped to a status such as Not started, In progress, or Completed.

Variables: project_name

## Prompt

Generate a JSON structure for maintaining a checklist used in code reviews of '{{project_name}}'. This will be a JSON object with key-value pairs where each pair represents an item on the checklist and its status. For example, an item might be 'Check for proper variable naming', and its status would be 'Not started', 'In progress' or 'Completed'.
