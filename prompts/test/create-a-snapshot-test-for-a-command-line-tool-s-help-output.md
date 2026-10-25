---
title: "Create a Snapshot Test for a Command-Line Tool's Help Output"
slug: create-a-snapshot-test-for-a-command-line-tool-s-help-output
stage: Test
category: "Testing & QA"
grade: B
score: 73
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-snapshot-test-for-a-command-line-tool-s-help-output
---
# Create a Snapshot Test for a Command-Line Tool's Help Output

Ensure consistent CLI documentation by generating snapshot tests and update scripts to validate help output against regressions.

Variables: programming_language

## Prompt

You are a developer building a command-line tool. Your task is to create a snapshot test for the help output of your tool to ensure that it is always up-to-date and accurate. The tool is written in {{programming_language}}.

Context:
- You want to prevent accidental changes to the help output, which could confuse the users.
- You are using a testing framework that supports snapshot testing.

Provide:
1. A test that runs your tool with the `--help` flag and creates a snapshot of the output.
2. A script to update the snapshot when the help output is intentionally changed.

## Tips

A simple but effective prompt for developers to ensure the quality of their command-line tools.
