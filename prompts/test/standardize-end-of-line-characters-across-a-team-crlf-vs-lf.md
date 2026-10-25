---
title: "Standardize End-of-Line Characters Across a Team (CRLF vs LF)"
slug: standardize-end-of-line-characters-across-a-team-crlf-vs-lf
stage: Test
category: "Cleanup & Warnings"
grade: C
score: 62
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/standardize-end-of-line-characters-across-a-team-crlf-vs-lf
---
# Standardize End-of-Line Characters Across a Team (CRLF vs LF)

Get an LF line-ending setup using .gitattributes and Git configuration guidance for teams seeing noisy diffs across Windows, macOS, and Linux.

## Prompt

My team has developers on both Windows and macOS/Linux. This is causing problems with Git because of different end-of-line characters (CRLF on Windows, LF on macOS/Linux). We see entire files being marked as changed in pull requests, which makes code reviews difficult.

Your task is to provide a simple, definitive solution to this problem that the whole team can adopt.

1.  **The Problem:** Briefly explain why different operating systems use different line endings and why this is a problem for Git.
2.  **The `.gitattributes` Solution:** Introduce the `.gitattributes` file as the primary solution. Provide a simple, universal `.gitattributes` file that will enforce LF line endings for all text files in the repository.
3.  **Configuring Git:** Explain the `core.autocrlf` Git configuration setting. Should developers set it to `true

## Tips

A classic problem for cross-platform teams. This prompt provides the standard, industry-accepted solution.
