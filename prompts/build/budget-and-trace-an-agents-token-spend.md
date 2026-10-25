---
title: "Budget and trace an agent's token spend"
slug: budget-and-trace-an-agents-token-spend
stage: Build
category: "AI Agent Development"
grade: C
score: 69
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/budget-and-trace-an-agents-token-spend
---
# Budget and trace an agent's token spend

Instrument an agent so every run reports cost per step and trips a budget before it overruns.

Variables: agent_name, monthly_budget

## Prompt

You are a backend engineer instrumenting an agent for cost control.

Context:
- The agent: {{agent_name}}
- The monthly budget it must respect: {{monthly_budget}}

Your task is to design the tracing and budgeting layer, and specify what it reports.

Steps:
1. Define the span model: one span per model call and per tool call, carrying model name, input and output tokens, latency, and outcome.
2. Define the run record that aggregates spans: total tokens, total cost, tool-call count, retries, and whether the run succeeded.
3. Specify the derived metric set, including cost per successful run and the retry share of spend.
4. Define budget enforcement: soft threshold behaviour, hard cap behaviour, and what the user sees when a run is refused.
5. Specify the top-line dashboard: at most six panels, each answering a named question.
6. Define the alert conditions and who receives them.

Constraints:
- Do not log prompt or completion bodies containing user data; log token counts and hashes.
- The budget check must run before the call, not after.
- Keep cardinality bounded: no per-user labels on metrics.

Output format, in Markdown: a **Span schema** and **Run record** in fenced code blocks, a metrics table with columns metric, formula, question answered, then **Budget enforcement** and **Alerts** as bulleted lists.

## Tips

Cost per successful task is the number that matters. Cost per call hides the retries.
