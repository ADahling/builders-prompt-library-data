---
title: "Multi-Agent System Design"
slug: multi-agent-system-design
stage: Build
category: "AI Agent Development"
grade: B
score: 77
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/multi-agent-system-design
---
# Multi-Agent System Design

Design a multi-agent system for a complex task with agent roles, prompts, tools, handoffs, orchestration, error handling, and evaluation.

## Prompt

Design a multi-agent system for [describe the complex task]:

1. AGENT DEFINITIONS: For each agent:
   - Name and role (e.g., "Researcher", "Analyst", "Writer")
   - System prompt with specific expertise
   - Tools available to this agent only
   - What it produces (output format)

2. ORCHESTRATION:
   - Which agent runs first?
   - How do agents pass information to each other?
   - What's the handoff format between agents?
   - Can agents run in parallel or must they be sequential?
   - Who makes the final decision if agents disagree?

3. COORDINATION PROMPT:
```
You are the Orchestrator. You coordinate [N] specialized agents:
- Agent 1: [role, when to invoke]
- Agent 2: [role, when to invoke]
- Agent 3: [role, when to invoke]

Given the user's request, determine:
1. Which agents need to be involved
2. In what order
3. What information each agent needs from the previous one
4. When to stop and return the final result
```

4. ERROR HANDLING:
   - What happens if an agent produces low-quality output?
   - Retry logic vs fallback agent
   - Timeout handling for long-running agents

5. EVALUATION: How to test if the multi-agent system produces better results than a single agent.

## Tips

Multi-agent systems are how you handle tasks too complex for a single prompt. Used by Devin, AutoGPT, and enterprise AI workflows. Source: augmentcode.com/blog/how-to-build-your-agent-11-prompting-techniques
