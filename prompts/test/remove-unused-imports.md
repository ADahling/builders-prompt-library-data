---
title: "Remove Unused Imports"
slug: remove-unused-imports
stage: Test
category: "Cleanup & Warnings"
grade: C
score: 64
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/remove-unused-imports
---
# Remove Unused Imports

Find unused imports in JavaScript and TypeScript files, with a list of affected files and code modifications to remove those imports.

Variables: directory_path

## Prompt

Analyze the JavaScript/TypeScript files within {{directory_path}} for any unused imports. Generate a list of files that contain these imports and provide the necessary code modifications to remove them safely.

## Tips

Removing unused imports helps to declutter your code and may improve performance.
