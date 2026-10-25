---
title: "Test an agent loop with recorded fixtures"
slug: test-an-agent-loop-with-recorded-fixtures
stage: Build
category: "AI Agent Development"
grade: B
score: 76
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/test-an-agent-loop-with-recorded-fixtures
---
# Test an agent loop with recorded fixtures

Build a deterministic test suite for an agent by recording tool responses and asserting on decisions.

Variables: agent_entrypoint, tool_list

## Prompt

You are a test engineer making an agent's behaviour reproducible in CI.

Context:
- The agent entry point: {{agent_entrypoint}}
- The tools it can call: {{tool_list}}

Your task is to design a fixture-based test suite that runs without network access and fails loudly on behaviour regressions.

Steps:
1. Define the recording format for a session: inputs, ordered tool calls with arguments, tool responses, and the final answer.
2. Specify the fixture harness: how recorded tool responses are replayed, and what happens when the agent calls a tool the fixture does not contain.
3. Write the assertion strategy. Assert on the sequence of tool calls and their arguments; assert on the final answer only through structural checks.
4. Enumerate the scenarios to record: happy path, tool error, empty result, ambiguous input, prompt injection in tool output, and the tool-call cap.
5. Define the flake policy: what makes a test non-deterministic and how the harness removes that source.
6. State the coverage report: which tools and which branches each scenario exercises.

Constraints:
- No live model calls in CI. Model responses are replayed or stubbed.
- No assertion on exact wording of natural-language output.
- Every scenario must fail for exactly one reason.

Output format, in Markdown: a **Fixture schema** code block, a scenarios table with columns scenario, trigger, expected tool sequence, pass condition, then **Harness notes** and **Flake policy** as bulleted lists.

## Tips

Assert on the tool calls the agent chooses, not on the prose it writes. Prose changes; decisions are the contract.
