---
title: "Systematically Refactor Promise Chains from .then() to async/await"
slug: systematically-refactor-promise-chains-from-then-to-async-await
stage: Test
category: "Cleanup & Warnings"
grade: C
score: 64
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/systematically-refactor-promise-chains-from-then-to-async-await
---
# Systematically Refactor Promise Chains from .then() to async/await

Get a guide to replacing promise chains with async/await, including before-and-after examples, automation options, and a testing workflow.

## Prompt

My JavaScript/TypeScript codebase is inconsistent in its handling of asynchronous operations. It has a mix of older `.then()`/`.catch()` promise chains and modern `async/await` syntax. I want to standardize the entire codebase to use `async/await` for better readability and error handling.

Your task is to provide a comprehensive guide for this refactoring effort. Please include:

1.  **Benefits of `async/await`:** Briefly explain the advantages of using `async/await` over `.then()` chains (e.g., linear code flow, simpler error handling).
2.  **Refactoring Patterns:** Provide clear "before" and "after" code examples for common patterns:
    *   A simple promise chain.
    *   A chain with a `.catch()` block.
    *   Using `Promise.all()`.
    *   Error handling with `try...catch` blocks.
3.  **Automated Tooling:** Can this refactoring be automated? Introduce ESLint rules (like `promise/prefer-await-to-then`) or codemods that can help identify and even automatically fix these patterns.
4.  **Step-by-Step Workflow:** Outline a safe, step-by-step process for a developer to follow when refactoring a file, including how to test the changes to ensure no logic has been altered.

Output should be a practical guide for modernizing an asynchronous codebase.

## Tips

This refactoring greatly improves the readability and maintainability of asynchronous code.
