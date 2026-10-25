---
title: "Onboarding Guide for New Developers"
slug: onboarding-guide-for-new-developers
stage: Design
category: "Documentation"
grade: A
score: 80
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/onboarding-guide-for-new-developers
---
# Onboarding Guide for New Developers

Write a project onboarding guide for developers with setup steps, a first PR, architecture, conventions, testing, deployment, contacts, and gotchas.

## Prompt

Create a developer onboarding guide for this project:

Project: [name and purpose]
Stack: [technologies]
Team size: [number]
Repo: [mono-repo / multi-repo]

Day 1 — Setup:
1. Access: What accounts/permissions to request (GitHub, cloud provider, monitoring, etc.)
2. Local environment: Step-by-step setup with expected output at each step
3. Common setup issues and solutions
4. First PR: A designated "good first issue" to verify everything works

Week 1 — Context:
5. Architecture overview: System diagram with data flow
6. Key abstractions: The 5-10 concepts a developer must understand
7. Code conventions: Naming, file structure, patterns used
8. Testing philosophy: What to test, how, minimum coverage
9. Deployment pipeline: How code gets to production

Ongoing:
10. Who to ask: Domain experts for each area
11. Decision log: Where to find past architectural decisions
12. Gotchas: Things that will confuse you and why they're that way

## Tips

A developer who ships their first PR in 2 days vs 2 weeks = onboarding quality.
