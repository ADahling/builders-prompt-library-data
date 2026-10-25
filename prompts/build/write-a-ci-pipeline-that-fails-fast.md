---
title: "Write a CI pipeline that fails fast"
slug: write-a-ci-pipeline-that-fails-fast
stage: Build
category: "DevOps & IaC"
grade: C
score: 69
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-a-ci-pipeline-that-fails-fast
---
# Write a CI pipeline that fails fast

Order CI stages by cost and signal so the cheapest check that can fail runs first.

Variables: repo_stack, current_pipeline

## Prompt

You are a build engineer restructuring a slow CI pipeline.

Context:
- The stack: {{repo_stack}}
- The pipeline today: {{current_pipeline}}

Your task is to reorder and reshape the pipeline so the median failing run reports in the shortest possible time.

Steps:
1. Inventory the current stages with their runtime and what class of failure each one catches.
2. Rank stages by cost per failure caught, cheapest first, and propose the new order.
3. Identify what can run in parallel without sharing mutable state, and what must stay sequential, with the reason.
4. Specify the caching strategy: what is cached, the cache key, and the invalidation rule.
5. Define the required checks that block merge, separate from the informational ones that do not.
6. State the target: median time to first failure, and total green-run time.

Constraints:
- Do not parallelise steps that share a lockfile, database, port, or output artifact.
- Every required check must be deterministic; move flaky checks out of the merge gate and say so.
- Do not add a stage without naming the failure class it catches.

Output format, in Markdown: a stages table with columns stage, runtime, catches, blocking, order; then the pipeline as a YAML code block; then **Caching** and **Targets** as bulleted lists.

## Tips

Order stages by cost divided by catch rate. A ten-second lint that catches half the failures belongs first.
