---
title: "Add guardrails to an agent that touches production"
slug: add-guardrails-to-an-agent-that-touches-production
stage: Build
category: "AI Agent Development"
grade: A
score: 81
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/add-guardrails-to-an-agent-that-touches-production
---
# Add guardrails to an agent that touches production

Wrap an agent's write path in approvals, dry runs, and audit records before it reaches live data.

Variables: agent_name, write_operations

## Prompt

You are a platform engineer hardening an agent that performs writes against production systems.

Context:
- The agent: {{agent_name}}
- The write operations it can perform: {{write_operations}}

Your task is to design the guardrail layer that sits between the agent's decision and the effect.

Steps:
1. Classify each write by blast radius: reversible, reversible with effort, irreversible. Say which tier requires human approval.
2. Specify a dry-run mode for every write: what it renders as a diff, and how the model presents it for approval.
3. Define the audit record: who or what triggered it, the arguments, the diff, the approver, and the outcome. Name where it is stored and how long it is kept.
4. Define the kill switch: how an operator halts the agent mid-run, and what state the system is left in.
5. Specify the rate and quota limits per operation, and the behaviour on breach.
6. List the failure modes this design does not cover, so nobody assumes full coverage.

Constraints:
- Never let the agent approve its own write, including by calling an approval tool.
- Every irreversible operation requires an explicit human confirmation carrying the diff hash.
- Assume tool output can be attacker-controlled and design accordingly.

Output format, in Markdown: a table of operations with columns operation, tier, approval, rate limit; then **Dry run**, **Audit record**, **Kill switch**, and **Uncovered failure modes** as sections.

## Tips

Dry run first, approval second, audit third. An agent that cannot show you the diff should not be applying it.
