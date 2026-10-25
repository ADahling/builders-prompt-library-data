---
title: "Audit and Enforce Architectural Boundaries with dep-cruiser"
slug: audit-and-enforce-architectural-boundaries-with-dep-cruiser
stage: Test
category: "Cleanup & Warnings"
grade: C
score: 65
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/audit-and-enforce-architectural-boundaries-with-dep-cruiser
---
# Audit and Enforce Architectural Boundaries with dep-cruiser

Your application has grown into a large monolith and the boundaries between its modules are blurry.

Variables: framework

## Prompt

My {{framework}} application has grown into a large monolith, and the boundaries between different modules are becoming blurry. I want to enforce a clear architectural separation between different parts of the application (e.g., the `core` logic should not depend on the `ui` framework).

I want to use `dependency-cruiser` to audit and enforce these architectural rules. Your task is to provide a comprehensive guide on how to do this.

1.  **Installation and Basic Setup:** How to install and run `dependency-cruiser` to generate an initial dependency graph.
2.  **Defining Architectural Rules:** How to write rules in the `.dependency-cruiser.js` configuration file to enforce architectural constraints. Provide examples for common scenarios:
    *   Forbidding `ui` modules from being imported by `core` modules.
    *   Allowing `feature` modules to depend on `core

## Tips

An essential tool for preventing a monolith from turning into a 'big ball of mud'. It enforces architecture as code.
