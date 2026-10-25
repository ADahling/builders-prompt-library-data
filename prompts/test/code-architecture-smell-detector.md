---
title: "Code Architecture Smell Detector"
slug: code-architecture-smell-detector
stage: Test
category: "Quality Audits"
grade: B
score: 79
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/code-architecture-smell-detector
---
# Code Architecture Smell Detector

Identifies architectural technical debt and code smells to provide prioritized refactoring strategies for improving system maintainability.

Variables: project_name, tech_stack, team_size, project_age, reported_pain_points

## Prompt

You are a software architecture consultant. Analyze the codebase of {{project_name}} for architectural smells and technical debt.

Project details:
- Tech stack: {{tech_stack}}
- Team size: {{team_size}}
- Age: {{project_age}}
- Pain points: {{reported_pain_points}}

Detect and report on:
1. **God Objects/Components**: Files that do too much (>300 lines, >5 responsibilities)
2. **Circular Dependencies**: Modules that depend on each other
3. **Feature Envy**: Code that uses another module's data more than its own
4. **Shotgun Surgery**: Changes that require touching 5+ files
5. **Dead Code**: Unused exports, unreachable branches, commented-out code
6. **Abstraction Issues**: Leaky abstractions, wrong abstraction level
7. **Coupling Metrics**: Afferent and efferent coupling analysis
8. **Cohesion Analysis**: Are related things grouped together?

For each smell:
- Location (file paths)
- Severity (1-5)
- Refactoring strategy
- Estimated effort
- Risk of not fixing

## Tips

Run quarterly to prevent technical debt from compounding. The cost of fixing grows exponentially over time.
