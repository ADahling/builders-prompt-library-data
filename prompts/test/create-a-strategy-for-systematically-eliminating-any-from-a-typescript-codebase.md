---
title: "Create a Strategy for Systematically Eliminating `any` from a TypeScript Codebase"
slug: create-a-strategy-for-systematically-eliminating-any-from-a-typescript-codebase
stage: Test
category: "Cleanup & Warnings"
grade: A
score: 87
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-strategy-for-systematically-eliminating-any-from-a-typescript-codebase
---
# Create a Strategy for Systematically Eliminating `any` from a TypeScript Codebase

Get a team strategy for replacing TypeScript any types, with usage tracking, prioritization, replacement patterns, and workflow guidance.

Variables: issue_tracker

## Prompt

My TypeScript project has a significant amount of "any" types, which defeats the purpose of using TypeScript. I want to launch a concerted effort to eliminate as many `any` types as possible and replace them with proper, specific types.

Your task is to create a detailed strategy document for "The Great `any` Purge." This document should guide the team through the process.

1.  **The Case Against `any`:** Start by explaining why `any` is detrimental to a TypeScript project. Discuss its impact on type safety, refactoring, and developer tooling (e.g., IntelliSense).
2.  **Finding and Tracking `any`:** How can we find all usages of `any`? Recommend ESLint rules (`@typescript-eslint/no-explicit-any`) and other tools to track the number of `any`s over time, creating a burndown chart.
3.  **Prioritization Strategy:** It's a big task. How should we prioritize? Suggest a strategy, for example:
    *   Start with the data layer and API boundaries.
    *   Focus on the most critical business logic first.
    *   Tackle modules with the highest `any` count.
4.  **Replacement Patterns:** Provide a "cookbook" of patterns for replacing `any`. Include examples for:
    *   Third-party library functions with no types.
    *   Complex API response objects.
    *   Functions that can accept multiple types of input.
    *   When to use `unknown` instead of `any`.
5.  **Team Workflow:** How to manage this as a team effort. Suggest creating a "type debt" backlog in `{{issue_tracker}}` and allocating time in each sprint to work on it.

Output should be a comprehensive and motivating strategy document.

## Tips

A challenging but highly rewarding initiative that dramatically improves the quality and robustness of a TypeScript project.
