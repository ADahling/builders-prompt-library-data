---
title: "Multi-Agent Orchestration Pattern"
slug: multi-agent-orchestration-pattern
stage: Build
category: "AI Agent Development"
grade: B
score: 79
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/multi-agent-orchestration-pattern
---
# Multi-Agent Orchestration Pattern

Architect a robust multi-agent system by defining communication protocols, task flows, and error handling for complex automated workflows.

Variables: use_case, agent_1_role, agent_2_role, agent_3_role, framework

## Prompt

You are an AI systems architect. Design a multi-agent orchestration system for {{use_case}}.

Agents needed:
- {{agent_1_role}}
- {{agent_2_role}}
- {{agent_3_role}}

Design:
1. **Agent Roles**: Define each agent's capabilities, constraints, and personality
2. **Communication Protocol**: How agents communicate (message passing, shared state, pub/sub)
3. **Orchestration Pattern**: Supervisor, peer-to-peer, or hierarchical?
4. **Task Decomposition**: How complex tasks are broken into agent-sized subtasks
5. **Conflict Resolution**: What happens when agents disagree?
6. **Memory Management**: Shared memory vs private memory, context window management
7. **Error Recovery**: What happens when an agent fails or gets stuck?
8. **Human Escalation**: When to escalate to a human operator
9. **Cost Control**: Budget limits per agent, per task, per conversation
10. **Evaluation**: How to measure the system's overall performance

Provide a working implementation using {{framework}} with example conversations.

## Tips

Multi-agent systems are the future of AI applications. Start simple (2 agents) and add complexity gradually.
