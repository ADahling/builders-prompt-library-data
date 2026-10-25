---
title: "Identify Deprecated Dependencies"
slug: identify-deprecated-dependencies
stage: Test
category: "Cleanup & Warnings"
grade: C
score: 60
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/identify-deprecated-dependencies
---
# Identify Deprecated Dependencies

Review your project's package.json for deprecated dependencies and get a list of affected packages with replacement suggestions.

Variables: project_path

## Prompt

Review the package.json file in {{project_path}} for any dependencies that are deprecated. List these dependencies along with their replacement suggestions.

## Tips

Keeping your dependencies updated helps to maintain a secure application.
