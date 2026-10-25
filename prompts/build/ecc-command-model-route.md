---
title: "ECC Command: /model-route"
slug: ecc-command-model-route
stage: Build
category: "AI Agent Development"
grade: B
score: 75
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/ecc-command-model-route
---
# ECC Command: /model-route

Model Route Command Recommend the best model tier for the current task by complexity and budget.

## Prompt

# Model Route Command

Recommend the best model tier for the current task by complexity and budget.

## Usage

`/model-route [task-description] [--budget low|med|high]`

## Routing Heuristic

- `haiku`: deterministic, low-risk mechanical changes
- `sonnet`: default for implementation and refactors
- `opus`: architecture, deep review, ambiguous requirements

## Required Output

- recommended model
- confidence level
- why this model fits
- fallback model if first attempt fails

## Arguments

$ARGUMENTS:
- `[task-description]` optional free-text
- `--budget low|med|high` optional

## Tips

Source: Everything Claude Code (ECC) — Command: /model-route
