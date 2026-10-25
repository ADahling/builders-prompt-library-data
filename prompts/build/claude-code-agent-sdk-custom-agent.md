---
title: "Claude Code Agent SDK \u2014 Custom Agent"
slug: claude-code-agent-sdk-custom-agent
stage: Build
category: "AI Agent Development"
grade: B
score: 71
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/claude-code-agent-sdk-custom-agent
---
# Claude Code Agent SDK — Custom Agent

Build a custom Claude agent for your chosen purpose, with a model selection, TypeScript tool definitions, and an agentic execution loop.

## Prompt

Build a custom AI agent using the Claude Code Agent SDK (Anthropic):

## 1. AGENT DEFINITION
- Agent name: [name]
- Purpose: [what it does]
- Model: choose a currently supported Claude model from the provider documentation and set CLAUDE_MODEL to its model ID.

## 2. TOOL REGISTRATION
```typescript
import Anthropic from "@anthropic-ai/sdk";

const client = new Anthropic();
const tools: Anthropic.Tool[] = [
  {
    name: "search_codebase",
    description: "Search files in the project for a pattern",
    input_schema: {
      type: "object",
      properties: {
        query: { type: "string", description: "Search pattern or regex" },
        file_type: { type: "string", description: "File extension filter" },
      },
      required: ["query"],
    },
  },
  // Add more tools...
];
```

## 3. AGENTIC LOOP
```typescript
async function runAgent(userMessage: string) {
  const messages: Anthropic.MessageParam[] = [
    { role: "user", content: userMessage },
  ];

  while (true) {
    const response = await client.messages.create({
      model: process.env.CLAUDE_MODEL!,
      max_tokens: 4096,
      system: "You are a [describe agent role]. Use tools to accomplish tasks step by step.",
      tools,
      messages,
    });

    // Process tool calls
    if (response.stop_reason === "tool_use") {
      const toolUse = response.content.find(b => b.type === "tool_use");
      const result = await executeToolCall(toolUse.name, toolUse.input);
      messages.push({ role: "assistant", content: response.content });
      messages.push({
        role: "user",
        content: [{ type: "tool_result", tool_use_id: toolUse.id, content: result }],
      });
    } else {
      return response.content; // Agent finished
    }
  }
}
```

## 4. ERROR & SAFETY
- Max iterations guard (prevent infinite loops)
- Tool execution sandboxing
- Cost tracking per agent run
- Human-in-the-loop confirmation for destructive actions

## 5. TESTING
- Unit test each tool independently
- Integration test the full loop with mock tools
- Eval harness: run agent on 10+ test cases, measure success rate

Apply this to build: [DESCRIBE YOUR AGENT]

## Tips

Based on Anthropic's official agent SDK patterns. The agentic loop with tool_use stop_reason is the core pattern for building autonomous agents.
