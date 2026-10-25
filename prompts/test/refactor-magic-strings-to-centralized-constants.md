---
title: "Refactor 'Magic Strings' to Centralized Constants"
slug: refactor-magic-strings-to-centralized-constants
stage: Test
category: "Cleanup & Warnings"
grade: B
score: 71
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/refactor-magic-strings-to-centralized-constants
---
# Refactor 'Magic Strings' to Centralized Constants

Get a guide to finding repeated string literals and replacing them with centralized constants, including regex search and linting guidance.

Variables: language

## Prompt

My codebase is littered with "magic strings." These are string literals that are used in multiple places for things like event names, action types, or keys, but they are not defined as constants. 

Example in my `{{language}}` code:
`if (user.role === 'admin') { ... }`
`const eventName = 'user_logged_in';`

This is error-prone (typos) and makes the code hard to maintain. I want to refactor all these magic strings into a centralized set of constants.

Your task is to provide a guide on how to do this effectively.

1.  **The Problem with Magic Strings:** Explain in more detail why magic strings are considered a code smell.
2.  **Finding Magic Strings:** How can I find all the magic strings in my codebase? Suggest a strategy using your code editor's search functionality with a regular expression to find repeated string literals.
3.  **Refactoring Process:** Provide a step-by-step refactoring process:
    *   Create a central `constants.ts` (or equivalent) file.
    *   For each set of related magic strings (e.g., user roles), create an `enum` or a plain object to hold them as constants (e.g., `export const UserRole = { ADMIN: 'admin', EDITOR: 'editor' };`).
    *   Replace all occurrences of the magic string in the codebase with a reference to the new constant (e.g., `if (user.role === UserRole.ADMIN) { ... }`).
4.  **ESLint Rule:** Show how to use an ESLint rule (like `no-magic-numbers

## Tips

A simple refactoring that significantly improves the robustness and maintainability of a codebase.
