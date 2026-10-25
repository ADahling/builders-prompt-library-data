---
title: "ReAct Agent Framework (Reason + Act)"
slug: react-agent-framework-reason-act
stage: Build
category: "AI Agent Development"
grade: B
score: 78
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/react-agent-framework-reason-act
---
# ReAct Agent Framework (Reason + Act)

Build a task-specific ReAct agent loop with tool calls, observations, iteration limits, and a complete three- to four-iteration example.

## Prompt

Implement a ReAct (Reasoning + Acting) agent loop for [describe the task]:

The agent should follow this loop:

1. THOUGHT: Analyze the current situation. What do I know? What do I need to find out? What's my plan?
2. ACTION: Choose a tool and execute it with specific parameters.
3. OBSERVATION: Process the tool's response. What did I learn?
4. REPEAT: Continue the Thought → Action → Observation loop until the task is complete.
5. FINAL ANSWER: Synthesize all observations into a complete response.

SYSTEM PROMPT:
```
You are an AI agent that solves problems step by step using the ReAct framework.

For each step, output in this exact format:
Thought: [Your reasoning about what to do next]
Action: [tool_name(parameters)]
Observation: [What the tool returned]

When you have enough information to answer:
Thought: I now have enough information to provide a final answer.
Final Answer: [Your complete response]

Available tools:
[LIST TOOLS]

Rules:
- Never skip the Thought step
- Maximum 10 iterations before providing best available answer
- If stuck in a loop, try a different approach
- Always verify critical facts with a tool rather than assuming
```

Show a complete example trace with 3-4 iterations for my specific task.

## Tips

ReAct is the most proven agent framework — used by LangChain, AutoGPT, and most production agents. The key is forcing explicit reasoning before each action. Source: medium.com/@sayalisureshkumbhar
