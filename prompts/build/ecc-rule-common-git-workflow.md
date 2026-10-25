---
title: "ECC Rule: Common Git Workflow"
slug: ecc-rule-common-git-workflow
stage: Build
category: "DevOps & IaC"
grade: C
score: 66
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/ecc-rule-common-git-workflow
---
# ECC Rule: Common Git Workflow

Draft typed commit messages and pull request summaries with test plans based on full branch history when preparing changes for review.

## Prompt

# Git Workflow

## Commit Message Format
```
<type>: <description>

<optional body>
```

Types: feat, fix, refactor, docs, test, chore, perf, ci

Note: Attribution disabled globally via ~/.claude/settings.json.

## Pull Request Workflow

When creating PRs:
1. Analyze full commit history (not just latest commit)
2. Use `git diff [base-branch]...HEAD` to see all changes
3. Draft comprehensive PR summary
4. Include test plan with TODOs
5. Push with `-u` flag if new branch

> For the full development process (planning, TDD, code review) before git operations,
> see [development-workflow.md](./development-workflow.md).

## Tips

Source: Everything Claude Code (ECC) — Rule: common/git-workflow
