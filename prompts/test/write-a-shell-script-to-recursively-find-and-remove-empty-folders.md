---
title: "Write a Shell Script to Recursively Find and Remove Empty Folders"
slug: write-a-shell-script-to-recursively-find-and-remove-empty-folders
stage: Test
category: "Cleanup & Warnings"
grade: A
score: 80
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-a-shell-script-to-recursively-find-and-remove-empty-folders
---
# Write a Shell Script to Recursively Find and Remove Empty Folders

Get a find one-liner, safety notes, and an older-system alternative to recursively delete empty folders in a project directory.

## Prompt

My project directory has a lot of empty folders left over from previous refactorings and deleted files. I want a simple script to clean them up.

Your task is to provide a shell script that recursively finds and deletes all empty directories within the current directory.

1.  **The Command:** Provide a one-liner command using `find` to do this. Explain each part of the command:
    *   `find .`
    *   `-type d`
    *   `-empty`
    *   `-delete`
2.  **Safety:** Is this command safe to run? What happens if a directory contains hidden files? (The `-empty` flag in modern `find` implementations correctly handles this).
3.  **Alternative Script:** For older systems that might not have the `-delete` flag, provide an alternative script using a `while` loop or `xargs`.

Output should be a very short and simple guide.

## Tips

A quick and satisfying cleanup script.
