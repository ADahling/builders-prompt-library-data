---
title: "Tool/Function Calling Schema Generator"
slug: tool-function-calling-schema-generator
stage: Build
category: "AI Agent Development"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/tool-function-calling-schema-generator
---
# Tool/Function Calling Schema Generator

Get JSON function schemas, usage guidelines, and success, edge, and error examples for external tools your AI agent needs to call.

## Prompt

Generate JSON schemas for external tools an AI agent can invoke. For each tool I describe, create:

1. FUNCTION DEFINITION:
```json
{
  "name": "tool_name",
  "description": "Clear, specific description of what this tool does and when to use it",
  "parameters": {
    "type": "object",
    "properties": {
      "param1": {
        "type": "string",
        "description": "What this parameter is and valid values"
      }
    },
    "required": ["param1"]
  }
}
```

2. USAGE GUIDELINES:
   - When should the agent choose this tool over others?
   - What are the preconditions (data needed before calling)?
   - What does the return value look like?
   - Common failure modes and how to handle them.

3. EXAMPLE CALLS:
   - Happy path with expected input/output
   - Edge case with unusual but valid input
   - Error case with invalid input

My tools to define: [describe your tools — e.g., "search a database", "send an email", "create a file", "call an external API"]

## Tips

Function calling schemas are how agents interact with external tools. Bad schemas = bad tool selection. Source: promptingguide.ai/agents/function-calling
