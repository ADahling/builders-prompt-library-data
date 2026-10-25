---
title: "Cleanup console.log Statements"
slug: cleanup-console-log-statements
stage: Test
category: "Cleanup & Warnings"
grade: C
score: 62
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/cleanup-console-log-statements
---
# Cleanup console.log Statements

Find console.log statements in a chosen codebase directory and get a list with suggestions to remove them or use a logging mechanism.

Variables: directory_path

## Prompt

Scan the codebase for all instances of console.log statements in the files under {{directory_path}}. Create a list of these statements and suggest either removing them or replacing them with a proper logging mechanism.

## Tips

This helps to clean up the code for production and improves maintainability.
