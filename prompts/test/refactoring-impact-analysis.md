---
title: "Refactoring Impact Analysis"
slug: refactoring-impact-analysis
stage: Test
category: "Code Review"
grade: A
score: 81
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/refactoring-impact-analysis
---
# Refactoring Impact Analysis

Get a refactoring impact analysis covering risks, dependencies, tests, migration, rollback, effort, and a recommendation before changing code.

## Prompt

Analyze the impact of this proposed refactoring:

Current code: [paste or describe current implementation]
Proposed change: [describe the refactoring]
Reason: [why refactor — tech debt, performance, readability]

Analyze:
1. Blast radius: What files/modules/services are affected?
2. Risk assessment: What could break? Rate likelihood and severity.
3. Dependencies: What depends on the code being changed? (imports, API contracts, database)
4. Backward compatibility: Any breaking changes for consumers?
5. Testing gap: What existing tests will break? What new tests are needed?
6. Migration: Is a data migration required? Can it be done with zero downtime?
7. Rollback plan: How to revert if something goes wrong?
8. Effort estimate: T-shirt size (S/M/L/XL) with justification.
9. Phased approach: Can this be broken into smaller, safer PRs?

Recommendation: Proceed / proceed with caution / defer / don't do it.

## Tips

Prevents 'simple refactor' PRs that break production.
