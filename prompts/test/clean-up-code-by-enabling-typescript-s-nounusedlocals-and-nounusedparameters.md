---
title: "Clean Up Code by Enabling TypeScript's `noUnusedLocals` and `noUnusedParameters`"
slug: clean-up-code-by-enabling-typescript-s-nounusedlocals-and-nounusedparameters
stage: Test
category: "Cleanup & Warnings"
grade: B
score: 78
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/clean-up-code-by-enabling-typescript-s-nounusedlocals-and-nounusedparameters
---
# Clean Up Code by Enabling TypeScript's `noUnusedLocals` and `noUnusedParameters`

Get a beginner guide to TypeScript's unused variable and parameter checks, with tsconfig setup, error fixes, and underscore conventions.

## Prompt

I want to keep my TypeScript codebase as clean as possible. I've noticed that there are many unused variables and function parameters, which add clutter and can be confusing.

I've heard that TypeScript has compiler options to detect these. Your task is to explain how to use them.

1.  **The Compiler Options:** Introduce the `noUnusedLocals` and `noUnusedParameters` compiler options in `tsconfig.json`. Explain what each one does.
2.  **Configuration:** Show how to enable these options in a `tsconfig.json` file.
3.  **Fixing the Errors:** When I enable these options, I get a lot of errors. What is the best way to fix them?
    *   For unused local variables, the fix is usually to just remove them.
    *   For unused parameters, it can be more complex. Explain how to use a leading underscore (e.g., `_unusedParam`) to signal to the compiler that the parameter is intentionally unused. When is this appropriate?
4.  **Benefits:** Briefly explain the benefits of enabling these flags (e.g., cleaner code, easier to spot bugs related to unused variables).

Output should be a simple and clear guide for a TypeScript beginner.

## Tips

A very easy and quick way to improve code quality in any TypeScript project.
