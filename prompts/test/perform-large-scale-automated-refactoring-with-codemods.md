---
title: "Perform Large-Scale Automated Refactoring with Codemods"
slug: perform-large-scale-automated-refactoring-with-codemods
stage: Test
category: "Cleanup & Warnings"
grade: A
score: 89
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/perform-large-scale-automated-refactoring-with-codemods
---
# Perform Large-Scale Automated Refactoring with Codemods

Get a step-by-step jscodeshift guide with transform code, import updates, and run commands for replacing a deprecated API across a codebase.

Variables: language, deprecated_api_usage, new_api_usage

## Prompt

I need to perform a large-scale refactoring across my entire {{language}} codebase. The change involves updating a deprecated API to a new one, and doing it manually would be time-consuming and error-prone. I want to use a codemod to automate this process.

Deprecated API usage: `{{deprecated_api_usage}}`
New API usage: `{{new_api_usage}}`

Your task is to provide a step-by-step guide to creating and running a codemod for this refactoring. Please use `jscodeshift`.

1.  **Introduction to Codemods:** Briefly explain what codemods are and why they are powerful for automated refactoring. Introduce `jscodeshift`.
2.  **Setting up the Environment:** How to install `jscodeshift` and set up a file for the codemod transform.
3.  **Writing the Transform:** Provide the complete JavaScript code for the `jscodeshift` transform. The code should:
    *   Find all occurrences of the deprecated API usage.
    *   Replace them with the new API usage.
    *   Handle any necessary import/export changes.
    *   Be well-commented to explain the logic, especially the part that interacts with the AST.
4.  **Running the Codemod:** The command to run the codemod on the entire codebase. Explain the different options, like `--dry` for a dry run and `-p` for printing the output.

Output should be a complete guide that allows a developer to confidently run a large-scale automated refactoring.

## Tips

Codemods are a superpower for developers, enabling massive, safe changes that would be impossible to do manually.
