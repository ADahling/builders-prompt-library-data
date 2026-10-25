---
title: "Write data quality tests for a pipeline"
slug: write-data-quality-tests-for-a-pipeline
stage: Build
category: "Modern Data Stack"
grade: A
score: 82
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-data-quality-tests-for-a-pipeline
---
# Write data quality tests for a pipeline

Define freshness, volume, schema, and distribution tests that catch a broken pipeline before a dashboard does.

Variables: pipeline_description, critical_tables

## Prompt

You are an analytics engineer adding tests to a pipeline that has been failing silently.

Context:
- The pipeline: {{pipeline_description}}
- The tables that decisions depend on: {{critical_tables}}

Your task is to define the smallest test suite that would have caught the failures nobody noticed.

Steps:
1. For each critical table, define the freshness test: expected update cadence, the allowed lag, and the timestamp column used.
2. Define volume tests: expected row-count range per run, and the rule for detecting a partial load.
3. Define schema tests: required columns, types, nullability, and uniqueness of keys.
4. Define referential tests between tables where a broken join would silently drop rows.
5. Add distribution tests only where a shift would change a decision, and name the decision.
6. Define severity and routing: which failures block downstream models and which only warn.

Constraints:
- Every test must be expressible as a query returning zero rows on pass.
- No test may depend on a hardcoded date.
- Keep the suite under twenty tests; say what you deliberately left untested.

Output format, in Markdown: a tests table with columns table, test, query sketch, severity, blocking; then **Deliberately untested** and **Routing** as bulleted lists.

## Tips

Freshness and row-count tests catch most real incidents. Add distribution tests only where a silent shift would mislead a decision.
