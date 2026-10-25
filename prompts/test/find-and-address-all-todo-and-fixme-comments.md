---
title: "Find and Address All TODO and FIXME Comments"
slug: find-and-address-all-todo-and-fixme-comments
stage: Test
category: "Cleanup & Warnings"
grade: A+
score: 92
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/find-and-address-all-todo-and-fixme-comments
---
# Find and Address All TODO and FIXME Comments

Get a workflow to find and categorize TODO and FIXME comments, choose fixes or issue tickets, and use editor tools to manage cleanup.

Variables: code_editor, issue_tracker

## Prompt

My codebase has accumulated many `TODO` and `FIXME` comments over time. I want to conduct a review of all these comments and either address them or create proper issues for them in our issue tracker.

Your task is to provide a workflow for this. Please include:

1.  **Finding Comments:** How to find all `TODO` and `FIXME` comments in the codebase using {{code_editor}}'s search functionality or a command-line tool like `grep`.
2.  **Categorization:** A simple framework for categorizing the comments. For example:
    *   **Quick Fix:** Can be addressed in under 30 minutes.
    *   **Feature Enhancement:** Represents a new feature or improvement.
    *   **Bug:** Represents a known bug.
    *   **Refactor:** Requires a larger code refactoring.
3.  **Action Plan:** For each category, what is the appropriate action? (e.g., "Fix it now," "Create a ticket in {{issue_tracker}}," "Discuss with the team").
4.  **Tooling:** Are there any extensions for {{code_editor}} that can help manage `TODO` comments? (e.g., Todo Tree).

Output should be a simple, actionable guide for a developer to systematically clean up these comments.

## Tips

A great way to turn code comments into actionable tasks and reduce technical debt.
