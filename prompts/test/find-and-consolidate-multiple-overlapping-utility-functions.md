---
title: "Find and Consolidate Multiple, Overlapping Utility Functions"
slug: find-and-consolidate-multiple-overlapping-utility-functions
stage: Test
category: "Cleanup & Warnings"
grade: C
score: 61
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/find-and-consolidate-multiple-overlapping-utility-functions
---
# Find and Consolidate Multiple, Overlapping Utility Functions

Plan a cleanup of overlapping utility functions with an audit, consolidation strategies, and codemods to update existing call sites.

## Prompt

My project has a `utils` directory that has grown organically over time. It now contains dozens of small utility functions, and I've discovered that there is a lot of overlap. For example, we have three different functions that all do slightly different versions of formatting a date.

`formatDate(date)`
`getFormattedDate(date, formatString)`
`prettyDate(date)`

This is confusing for developers and a violation of the DRY (Don't Repeat Yourself) principle. I want to clean this up.

Your task is to provide a refactoring plan for consolidating these utility functions.

1.  **Audit:** How to audit the `utils` directory to find all the overlapping functions. Suggest a process of manually reviewing the functions and grouping them by functionality (e.g., date formatting, string manipulation, array operations).
2.  **Consolidation Strategy:** For each group of overlapping functions, propose a strategy for consolidating them into a single, more robust function. The new function should take options to handle the variations that the old functions supported. For the date example, the new function might be `formatDate(date, options)`.
3.  **Refactoring with Codemods:** This could be a lot of manual work. Explain how a codemod could be used to automatically find all the call sites of the old functions and replace them with a call to the new, consolidated function.
4.  **Using a Utility Library:** Is it possible that we are just reinventing the wheel? For common operations like date formatting and array manipulation, suggest that we should consider replacing our custom utility functions with a well-tested, standard library like `lodash` or `date-fns`.

Output should be a guide to cleaning up a messy `utils` directory.

## Tips

A common problem in long-running projects. This refactoring improves code quality and can often reduce the amount of custom code the team needs to maintain.
