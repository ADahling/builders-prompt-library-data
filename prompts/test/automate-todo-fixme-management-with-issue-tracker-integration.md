---
title: "Automate TODO/FIXME Management with Issue Tracker Integration"
slug: automate-todo-fixme-management-with-issue-tracker-integration
stage: Test
category: "Cleanup & Warnings"
grade: B
score: 79
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/automate-todo-fixme-management-with-issue-tracker-integration
---
# Automate TODO/FIXME Management with Issue Tracker Integration

Design a TODO/FIXME issue-tracker integration with parsing and API code, metadata handling, duplicate prevention, and comment-to-issue links.

Variables: issue_tracker

## Prompt

I want to automate the process of managing `TODO` and `FIXME` comments in my project. The goal is to automatically create issues in {{issue_tracker}} from these comments and keep them in sync.

Your task is to design a system for this. Please consider:

1.  **Comment Parsing:** How to parse `TODO` comments that contain metadata, such as an assignee and a due date (e.g., `// TODO(john.doe): Fix this by 2024-12-31`).
2.  **Issue Creation:** A script (e.g., a pre-commit hook or a CI job) that scans the codebase for new `TODO` comments and uses the {{issue_tracker}} API to create corresponding issues. The issue description should include the comment, the file path, and a link to the code.
3.  **Synchronization:** How to prevent duplicate issues from being created. The script should be able to associate a `TODO` comment with an existing issue.
4.  **Comment-to-Issue Linking:** After an issue is created, the script should update the `TODO` comment with the issue number (e.g., `// TODO(#123): ...`).

Provide a detailed design for this system, including code snippets for the parsing and API interaction logic.

## Tips

This bridges the gap between code comments and formal project management, ensuring that `TODO`s don't get lost.
