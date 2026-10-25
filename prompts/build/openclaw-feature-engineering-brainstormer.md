---
title: "OpenClaw: Feature Engineering Brainstormer"
slug: openclaw-feature-engineering-brainstormer
stage: Build
category: "OpenClaw"
grade: A+
score: 93
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-feature-engineering-brainstormer
---
# OpenClaw: Feature Engineering Brainstormer

Feature Engineering Brainstormer — OpenClaw Workflow Prompt Trigger Activate when a prediction problem is described or when asked to brainstorm features.

Variables: Generate 5+ features specific to the described domain, name, how to compute, why this might predict the target, best for tree-based / linear / both, Yes/No — explanation

## Prompt

# Feature Engineering Brainstormer — OpenClaw Workflow Prompt

## Trigger
Activate when a prediction problem is described or when asked to brainstorm features.

## Input Required
- Target variable: What are we predicting?
- Raw features: What data is available?
- Domain: What industry/context?
- Model type: Tree-based? Linear? Neural?

## Feature Generation Framework

### 1. Aggregation Features
- Group-by aggregations: count, sum, mean, median, min, max, std
- Rolling windows: 7-day, 30-day, 90-day aggregations
- Lag features: value at t-1, t-7, t-30
- Cumulative features: running totals, streaks

### 2. Time-Based Features
- Day of week, month, quarter, year
- Time since last event
- Time between events (inter-arrival time)
- Cyclical encoding (sin/cos for hour, day of week)
- Holiday/weekend flags
- Business days vs. calendar days

### 3. Interaction Features
- Ratios between numeric features (A/B, A-B)
- Cross-feature combinations (category × numeric)
- Polynomial features for key predictors
- Difference from group mean

### 4. Statistical Encodings
- Target encoding (with proper cross-validation)
- Frequency encoding
- Weight of evidence (WOE)
- Leave-one-out encoding

### 5. Domain-Inspired Features
- {{Generate 5+ features specific to the described domain}}
- Based on subject-matter knowledge patterns

## Output Format
For each feature:
```
Feature: {{name}}
Formula: {{how to compute}}
Intuition: {{why this might predict the target}}
Model fit: {{best for tree-based / linear / both}}
⚠️ Leakage risk: {{Yes/No — explanation}}
```

Generate 15+ feature ideas. Flag any leakage risks prominently.

## Tips

Generates 15+ feature ideas with leakage risk flags and model suitability tags. From Analytics Vidhya's 20 OpenClaw Prompts.
