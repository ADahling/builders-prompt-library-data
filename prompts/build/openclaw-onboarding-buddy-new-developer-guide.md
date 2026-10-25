---
title: "OpenClaw: Onboarding Buddy \u2014 New Developer Guide"
slug: openclaw-onboarding-buddy-new-developer-guide
stage: Build
category: "OpenClaw"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-onboarding-buddy-new-developer-guide
---
# OpenClaw: Onboarding Buddy — New Developer Guide

Get a developer onboarding plan tailored to your project, stack, and role, covering setup, architecture, first contributions, and ownership.

Variables: project, stack, size, role

## Prompt

# Onboarding Buddy — New Developer Guide Generator

## Input
- Project/repo name: {{project}}
- Tech stack: {{stack}}
- Team size: {{size}}
- New hire role: {{role}}

## Week 1: Environment & Context
### Day 1-2: Setup
- [ ] Clone repos and verify build
- [ ] Install required tools and extensions
- [ ] Set up local development environment
- [ ] Access: GitHub, CI/CD, monitoring, Slack channels
- [ ] Run the test suite — everything should pass

### Day 3-4: Architecture Tour
- [ ] Read architecture overview doc
- [ ] Walk through request lifecycle (API call → DB → response)
- [ ] Identify: entry points, core services, data models, external integrations
- [ ] Review deployment pipeline (commit → staging → production)

### Day 5: First Contribution
- [ ] Pick a "good first issue" (labeled, scoped, reviewed)
- [ ] Submit PR following team conventions
- [ ] Get review from onboarding buddy

## Week 2: Depth
- [ ] Read 5 recent PRs to understand code style and review culture
- [ ] Shadow an on-call rotation
- [ ] Pair program on a medium-complexity feature
- [ ] Write or update one piece of documentation

## Week 3-4: Independence
- [ ] Own a feature end-to-end (design → implement → ship)
- [ ] Participate in sprint planning
- [ ] Give first code review
- [ ] Present a lightning talk on something learned

## Onboarding Checklist Generator
For the given tech stack, auto-generate:
- Required tool installations
- Environment variable setup
- Database seeding instructions
- Common gotchas and troubleshooting
- Key contacts for different areas

## Tips

Generates structured onboarding plans for new developers. Covers environment setup, architecture tours, and progressive independence milestones.
