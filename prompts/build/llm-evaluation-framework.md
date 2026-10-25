---
title: "LLM Evaluation Framework"
slug: llm-evaluation-framework
stage: Build
category: "LLM & AI Integration"
grade: B
score: 79
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/llm-evaluation-framework
---
# LLM Evaluation Framework

Design an evaluation framework for an LLM feature with datasets, metrics, scoring rubrics, regression checks, and three example evaluations.

## Prompt

Create an evaluation framework for this LLM-powered feature:

Feature: [what the LLM does in your app]
Current model: [model name]
Success criteria: [what "good" looks like]

Framework:
1. Test dataset: How to build a golden dataset of input/expected-output pairs (minimum 50-100 cases)
2. Metrics:
   - Accuracy: Does the output match expected? (exact match, fuzzy, semantic similarity)
   - Relevance: Is the output useful for the user's intent?
   - Safety: Does it avoid harmful/biased/hallucinated content?
   - Latency: Response time at p50, p95, p99
   - Cost: Per-query cost at current and projected volume
3. Automated evaluation: Use an LLM-as-judge? Rubric for the judge?
4. Human evaluation: Sample size, annotator agreement, labeling interface?
5. Regression testing: How to detect quality degradation when changing prompts or models?
6. A/B testing: How to compare two prompt versions in production?
7. Monitoring: What to track in production (thumbs up/down, regeneration rate, abandonment)?

Provide a scoring rubric and example evaluation for 3 test cases.

## Tips

If you can't measure LLM quality, you can't improve it.
