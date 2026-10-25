---
title: "OpenClaw: Agile Product Owner Toolkit"
slug: openclaw-agile-product-owner-toolkit
stage: Build
category: "OpenClaw"
grade: B
score: 73
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-agile-product-owner-toolkit
---
# OpenClaw: Agile Product Owner Toolkit

Agile Product Owner — Backlog & Sprint Toolkit User Story Generation INVEST-compliant Template: As a persona , I want to action , So that benefit .

## Prompt

# Agile Product Owner — Backlog & Sprint Toolkit

## User Story Generation (INVEST-compliant)
Template: As a [persona], I want to [action], So that [benefit].

Story Types:
| Type | Template |
|------|----------|
| Feature | As a [persona], I want to [action] so that [benefit] |
| Improvement | As a [persona], I need [capability] to [goal] |
| Bug Fix | As a [persona], I expect [behavior] when [condition] |
| Enabler | As a developer, I need to [task] to enable [capability] |

## Acceptance Criteria (Given-When-Then)
Given [precondition], When [action], Then [expected outcome].

Checklist per story: Happy Path, Validation, Error Handling, Performance (<2s), Accessibility (keyboard nav)

Minimum AC by size: 1-2 pts → 3-4 criteria | 3-5 pts → 4-6 | 8 pts → 5-8 | 13+ → Split the story

## Epic Breakdown
Splitting Techniques:
- By workflow step: "Checkout" → "Add to cart" + "Enter payment" + "Confirm"
- By persona: "Dashboard" → "Admin dashboard" + "User dashboard"
- By data type: "Import" → "Import CSV" + "Import Excel"
- Happy path first: "Feature" → "Basic flow" + "Error handling" + "Edge cases"

## Sprint Planning
Sprint Capacity = Average Velocity × Availability Factor
- Committed: 85% of adjusted capacity
- Stretch: 15% additional

## Backlog Prioritization
| Factor | Weight |
|--------|--------|
| Value | 40% |
| Effort | 20% |
| Urgency | 20% |
| Risk | 10% |
| Learning | 10% |

## Tips

Backlog management and sprint execution toolkit. User story generation, acceptance criteria patterns, epic breakdown, sprint planning. From Rezvani's claude-skills.
