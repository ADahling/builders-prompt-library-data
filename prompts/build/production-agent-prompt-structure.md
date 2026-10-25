---
title: "Production Agent Prompt Structure"
slug: production-agent-prompt-structure
stage: Build
category: "AI Agent Development"
grade: A+
score: 95
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/production-agent-prompt-structure
---
# Production Agent Prompt Structure

Design an AI agent prompt with task steps, tool signatures, constraints, JSON output, and error handling for a specific role.

## Prompt

Design a production-ready AI agent prompt using this structure:

## ROLE
You are a [specific role] agent. Your purpose is [one sentence].

## TASK
Given [input], you must:
1. [Step 1 with specific action]
2. [Step 2 with specific action]
3. [Step 3 with specific action]

## TOOLS AVAILABLE
You have access to these tools:
- tool_name(param1: type, param2: type) → return_type: Description of what this tool does and when to use it.
- [List all tools with exact signatures]

## CONSTRAINTS
- Never [specific prohibition]
- Always [specific requirement]
- If uncertain about [scenario], ask the user rather than guessing.
- Maximum [N] tool calls per request.

## RESPONSE FORMAT
Return your response as:
```json
{
  "reasoning": "Your step-by-step thought process",
  "action": "The tool you're calling and why",
  "result": "The final answer or output",
  "confidence": "high | medium | low"
}
```

## ERROR HANDLING
- If a tool call fails: [specific recovery strategy]
- If the input is ambiguous: [specific clarification approach]
- If the task is outside your scope: [specific escalation path]

## Tips

From Reddit r/AI_Agents — this is the structure real production agents use. The key insight is separating Role, Task, Tools, and Constraints into distinct sections. Source: reddit.com/r/AI_Agents/comments/1l9zbvg
