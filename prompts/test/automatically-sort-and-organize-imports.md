---
title: "Automatically Sort and Organize Imports"
slug: automatically-sort-and-organize-imports
stage: Test
category: "Cleanup & Warnings"
grade: B
score: 73
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/automatically-sort-and-organize-imports
---
# Automatically Sort and Organize Imports

Get a TypeScript import-sorting guide with tool recommendations, ESLint configuration, path aliases, custom groups, and pre-commit automation.

## Prompt

My TypeScript project has inconsistent import statements. Some are unsorted, some have long relative paths, and the grouping is not consistent. I want to automate the process of organizing and sorting imports to improve code readability and maintainability.

Your task is to recommend and configure a tool for this. Please cover:

1.  **Tool Recommendation:** Recommend a tool for automatically sorting and organizing imports in a TypeScript project. The official ESLint plugin for imports (`eslint-plugin-import`) is a good candidate. Explain why this tool is a good choice.
2.  **Configuration:** Provide a sample ESLint configuration that enforces a specific import order. The order should be: 1) built-in modules, 2) external packages, 3) internal modules (with path aliases). Show how to configure path aliases in both `tsconfig.json` and the ESLint config.
3.  **Automation:** How to run the import sorting automatically. Explain how to integrate this with a pre-commit hook using `husky` and `lint-staged`.
4.  **Custom Groups:** How to define custom groups for imports, for example, to separate React components from utility functions.

Output should be a guide with the necessary configuration files and commands.

## Tips

Clean and organized imports make a huge difference in code navigation and understanding.
