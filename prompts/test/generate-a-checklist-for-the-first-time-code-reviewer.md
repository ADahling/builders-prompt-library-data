---
title: "Generate a checklist for the first-time code reviewer"
slug: generate-a-checklist-for-the-first-time-code-reviewer
stage: Test
category: "Code Review"
grade: A+
score: 91
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-a-checklist-for-the-first-time-code-reviewer
---
# Generate a checklist for the first-time code reviewer

Get a Markdown checklist for first-time reviewers covering code style, bugs, console logging, reuse, and stack-specific concerns.

Variables: tech_stack

## Prompt

We'd like to help first-time code reviewers understand what they should be looking for. Assist by generating a clear, organized checklist for reviewing {{tech_stack}} code. This checklist should cover general topics such as code style, bug detection, console logging oversight, and reuse of code, as well as any particulars for {{tech_stack}}. Validate the list items before export. The output should be a bulleted markdown list.
