---
title: "Write a Git Commit Message"
slug: write-a-git-commit-message
stage: Build
category: "AI Coding Assistants"
grade: B
score: 76
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-a-git-commit-message
---
# Write a Git Commit Message

Generate a concise, standardized Git commit message based on specific code changes and their classification.

Variables: change_summary, change_type

## Prompt

You are an AI coding assistant. Write a conventional Git commit message for the following changes:

Changes:
- {{change_summary}}

Type of change: {{change_type}} (e.g., feat, fix, chore)

## Tips

Helps enforce good Git practices from the beginning.
