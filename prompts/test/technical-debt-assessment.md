---
title: "Technical Debt Assessment"
slug: technical-debt-assessment
stage: Test
category: "Code Review"
grade: A+
score: 90
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/technical-debt-assessment
---
# Technical Debt Assessment

Analyze codebase architecture and infrastructure to generate a prioritized, risk-based remediation roadmap for resolving multi-layered technical debt.

Variables: project_name, project_age, team_size, deploy_frequency, pain_points

## Prompt

You are a technical debt analyst. Assess the technical debt in {{project_name}} and create a remediation plan.

Project context:
- Age: {{project_age}}
- Team size: {{team_size}}
- Deployment frequency: {{deploy_frequency}}
- Known pain points: {{pain_points}}

Assess:
1. **Dependency Debt**: Outdated packages, security vulnerabilities, deprecated APIs
2. **Architecture Debt**: Monolith that should be split, missing abstractions, tight coupling
3. **Code Debt**: Duplicated code, complex functions, missing types
4. **Test Debt**: Missing tests, flaky tests, slow test suite
5. **Documentation Debt**: Missing docs, outdated docs, tribal knowledge
6. **Infrastructure Debt**: Manual deployments, missing monitoring, no disaster recovery

For each debt item:
- Severity: Critical / High / Medium / Low
- Impact: What problems does it cause today?
- Risk: What could go wrong if not addressed?
- Effort: T-shirt size (S/M/L/XL)
- Recommendation: Fix now, schedule, or accept

Create a prioritized remediation roadmap with quarterly milestones.

## Tips

Technical debt compounds like financial debt. Regular assessment prevents it from becoming unmanageable.
