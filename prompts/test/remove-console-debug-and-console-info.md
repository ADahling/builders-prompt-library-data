---
title: "Remove Console.debug and Console.info"
slug: remove-console-debug-and-console-info
stage: Test
category: "Cleanup & Warnings"
grade: C
score: 63
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/remove-console-debug-and-console-info
---
# Remove Console.debug and Console.info

Find console.debug and console.info calls in a codebase, with a list of instances and suggestions to remove them or use a logging utility.

Variables: directory_path

## Prompt

Scan the codebase in {{directory_path}} for instances of console.debug and console.info. Generate a list of these instances and suggest either removing them or replacing them with a proper logging utility.

## Tips

This ensures that your production code is clean and avoids unnecessary log outputs.
