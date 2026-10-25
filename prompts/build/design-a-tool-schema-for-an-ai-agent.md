---
title: "Design a tool schema for an AI agent"
slug: design-a-tool-schema-for-an-ai-agent
stage: Build
category: "AI Agent Development"
grade: A
score: 82
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-a-tool-schema-for-an-ai-agent
---
# Design a tool schema for an AI agent

Specify agent tools with typed arguments, refusal cases, and error shapes the model can recover from.

Variables: agent_purpose, available_apis

## Prompt

You are a systems engineer designing the tool surface for an LLM agent.

Context:
- What the agent is for: {{agent_purpose}}
- Backing APIs and data it may reach: {{available_apis}}

Your task is to specify a minimal tool set the model can use correctly on the first attempt.

Steps:
1. Derive the smallest set of tools that covers the purpose. Merge tools that would always be called together; split any tool with a mode flag.
2. For each tool, define a JSON schema: name, one-sentence description written for the model, typed arguments with constraints, and the return shape.
3. Define the error contract. Every failure returns a machine-readable code plus a sentence telling the model what to do next.
4. State the refusal cases: inputs the tool must reject rather than guess at, and the exact message it returns.
5. List the idempotency and rate-limit properties of each write tool, and how a retry must behave.

Constraints:
- No tool may take free-text where an enum will do.
- No tool may perform a destructive write without an explicit confirmation argument.
- Do not expose raw database access or arbitrary code execution.

Output format, in Markdown: one section per tool containing the JSON schema in a fenced code block, followed by **Errors**, **Refusals**, and **Retry semantics** as bulleted lists. Close with a table of tools ordered by blast radius.

## Tips

Agents fail at the tool boundary far more often than at the reasoning step. Spend your effort on the schema.
