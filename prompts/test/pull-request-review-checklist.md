---
title: "Pull Request Review Checklist"
slug: pull-request-review-checklist
stage: Test
category: "Code Review"
grade: A
score: 85
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/pull-request-review-checklist
---
# Pull Request Review Checklist

Generate a customized senior-level code review checklist tailored to specific project stacks to ensure quality, security, and performance.

Variables: project_name, tech_stack

## Prompt

You are a senior developer. Generate a comprehensive pull request review checklist for {{project_name}} ({{tech_stack}}).

The checklist should cover:

**Code Quality:**
- [ ] Code follows project style guide
- [ ] No unnecessary complexity or over-engineering
- [ ] Functions/methods are single-responsibility
- [ ] Variable and function names are descriptive
- [ ] No magic numbers or hardcoded strings

**Functionality:**
- [ ] Code does what the PR description says
- [ ] Edge cases are handled
- [ ] Error handling is appropriate
- [ ] No regressions in existing functionality

**Security:**
- [ ] No secrets or credentials in code
- [ ] Input validation on all user inputs
- [ ] SQL injection prevention
- [ ] XSS prevention
- [ ] Authorization checks in place

**Performance:**
- [ ] No N+1 queries
- [ ] No unnecessary re-renders
- [ ] Large lists are virtualized
- [ ] Images are optimized

**Testing:**
- [ ] Unit tests for new logic
- [ ] Integration tests for new endpoints
- [ ] Edge case tests
- [ ] Test coverage maintained or improved

**Documentation:**
- [ ] Code comments for complex logic
- [ ] API documentation updated
- [ ] README updated if needed

Customize this for your project's specific needs.

## Tips

Consistent PR reviews catch bugs early and maintain code quality across the team.
