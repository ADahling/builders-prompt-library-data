---
title: "Refactor Legacy Callback-Based Asynchronous Code to use Promises"
slug: refactor-legacy-callback-based-asynchronous-code-to-use-promises
stage: Test
category: "Cleanup & Warnings"
grade: B
score: 71
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/refactor-legacy-callback-based-asynchronous-code-to-use-promises
---
# Refactor Legacy Callback-Based Asynchronous Code to use Promises

Modernize legacy Node.js code by refactoring nested error-first callbacks into clean, maintainable Promise chains and async/await syntax.

## Prompt

I am working on an older Node.js codebase that uses the traditional error-first callback pattern for asynchronous operations. This has led to "callback hell" (deeply nested callbacks) which is very hard to read and maintain.

Example:
`fs.readFile('file1.txt', (err, data1) => { ... });`

I want to refactor this code to use modern Promises, which will allow me to then use `async/await`.

Your task is to provide a guide on how to do this.

1.  **Callback Hell Explained:** Show a clear example of "callback hell" to illustrate the problem.
2.  **Promisification:** Explain the concept of "promisification." How do you wrap a function that takes a callback and make it return a Promise instead? Provide a generic `promisify` helper function that can do this.
3.  **Using `util.promisify`:** Introduce Node.js's built-in `util.promisify` as the standard way to do this for Node's own callback-based APIs (like the `fs` module).
4.  **Refactoring Example:** Provide a complete "before" and "after" example. Show a piece of code that uses nested callbacks to read multiple files, and then show the refactored version that uses Promises and `.then()` chains or `Promise.all()`.

Output should be a guide to modernizing a legacy Node.js codebase.

## Tips

A fundamental refactoring for any developer working on older Node.js code.
