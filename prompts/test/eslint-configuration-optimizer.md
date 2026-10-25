---
title: "ESLint Configuration Optimizer"
slug: eslint-configuration-optimizer
stage: Test
category: "Cleanup & Warnings"
grade: A
score: 85
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/eslint-configuration-optimizer
---
# ESLint Configuration Optimizer

Engineers a high-performance ESLint configuration to resolve team pain points and enforce strict code quality through automated standards.

Variables: project_name, framework, typescript_version, current_config, pain_points

## Prompt

You are a code quality engineer. Optimize the ESLint configuration for {{project_name}} to enforce consistent code quality.

Current setup:
- Framework: {{framework}}
- TypeScript: {{typescript_version}}
- Current ESLint config: {{current_config}}
- Team pain points: {{pain_points}}

Provide:
1. **Base Configuration**: Recommended extends (eslint:recommended, typescript-eslint, react-hooks, etc.)
2. **Custom Rules**: Project-specific rules with justification for each
3. **Import Ordering**: Consistent import grouping and sorting
4. **Naming Conventions**: Enforce naming patterns for components, hooks, utilities
5. **Complexity Limits**: Max cyclomatic complexity, max function length, max file length
6. **Security Rules**: no-eval, no-implied-eval, no-new-Function
7. **Performance Rules**: no-unnecessary-re-renders, memo requirements
8. **Auto-Fix**: Which rules can be auto-fixed on save
9. **CI Integration**: How to run ESLint in CI with proper caching
10. **Migration Plan**: How to enable strict rules gradually without blocking the team

## Tips

A well-configured linter catches bugs before they reach code review. Auto-fix on save eliminates style debates.
