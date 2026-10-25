---
title: "OpenClaw: Git Workflow & Branch Strategy Advisor"
slug: openclaw-git-workflow-branch-strategy-advisor
stage: Build
category: "OpenClaw"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-git-workflow-branch-strategy-advisor
---
# OpenClaw: Git Workflow & Branch Strategy Advisor

Get Git branching recommendations and commit conventions based on your team size, release cadence, environments, and workflow pain points.

Variables: size, frequency, envs, pain_points

## Prompt

# Git Workflow & Branch Strategy Advisor

## Input
- Team size: {{size}}
- Release frequency: {{frequency}} (continuous / weekly / monthly / quarterly)
- Environment count: {{envs}} (dev / staging / production)
- Current pain points: {{pain_points}}

## Strategy Recommendations

### Trunk-Based Development (Recommended for CI/CD)
Best for: Small-medium teams, continuous deployment
```
main ─────●─────●─────●─────●───── (always deployable)
           \   /       \   /
            ●─●         ●─●        (short-lived feature branches, <2 days)
```
Rules:
- Feature branches live <2 days
- All commits to main are deployable
- Use feature flags for incomplete features
- Require PR review + CI pass before merge

### GitHub Flow
Best for: Open source, small teams, simple release process
```
main ─────────●───────●───────── (deploy from main)
         \       /        
          ●──●──●              (feature/fix-login)
```

### Git Flow
Best for: Scheduled releases, multiple versions in production
```
main ────●────────────●──── (production releases only)
         |            |
develop ─●──●──●──●───●──── (integration branch)
             \  /
              ●●              (feature branches)
```

## Commit Message Convention
```
type(scope): description

Types: feat, fix, docs, style, refactor, perf, test, chore
Scope: component or area affected
Description: imperative mood, <72 chars

Examples:
feat(auth): add OAuth2 login with Google
fix(cart): prevent duplicate item addition
docs(api): update rate limit documentation
```

## PR Best Practices
- Keep PRs <400 lines of code
- One logical change per PR
- Include: what, why, how, testing steps
- Link to issue/ticket
- Add screenshots for UI changes
- Request review from code owner + one other

## Tips

Recommends git branching strategies based on team size and release cadence. Covers trunk-based, GitHub Flow, and Git Flow with commit conventions.
