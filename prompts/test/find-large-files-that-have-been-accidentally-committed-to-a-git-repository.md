---
title: "Find Large Files That Have Been Accidentally Committed to a Git Repository"
slug: find-large-files-that-have-been-accidentally-committed-to-a-git-repository
stage: Test
category: "Cleanup & Warnings"
grade: B
score: 78
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/find-large-files-that-have-been-accidentally-committed-to-a-git-repository
---
# Find Large Files That Have Been Accidentally Committed to a Git Repository

Get a shell script to diagnose Git repository bloat by listing the 20 largest files in history, their sizes, and the commits that added them.

## Prompt

My project's Git repository is very large, and `git clone` takes a long time. I suspect that someone has accidentally committed large binary files (like videos, PSDs, or database backups) to the repository's history.

I need a way to find these large files so I can remove them from the repository's history.

Your task is to provide a script or command to do this.

1.  **The Problem:** Explain why committing large files to Git is a bad idea (it bloats the repository for everyone, forever).
2.  **The Script:** Provide a shell script that uses `git rev-list` and `git cat-file` to search the entire history of the repository and list the largest files. The script should output a sorted list of the top 20 largest files, their sizes, and the commit they were added in.
3.  **Using `git-filter-repo`:** Finding the files is the first step. The next step is to remove them. Briefly introduce the `git-filter-repo` tool as the modern, recommended way to remove files from a repository's history. (This prompt is just about *finding* the files, but it should point to the solution).

Output should be a practical script for diagnosing a bloated Git repository.

## Tips

A common Git maintenance task. This script is a very useful diagnostic tool.
