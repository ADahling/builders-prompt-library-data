---
title: "Agentic Workflow Orchestration"
slug: agentic-workflow-orchestration
stage: Build
category: "AI Agent Development"
grade: A
score: 84
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/agentic-workflow-orchestration
---
# Agentic Workflow Orchestration

Design an agent workflow for an end-to-end process with a DAG, node roles, JSON schemas, shared state, retries, timeouts, and cost limits.

## Prompt

Design an agentic workflow for [describe end-to-end process]:

## 1. WORKFLOW GRAPH
Map the workflow as a directed acyclic graph (DAG):
- Node 1: [task] → triggers Node 2, Node 3
- Node 2: [task] → triggers Node 4
- Node 3: [task] → triggers Node 4
- Node 4: [task] → final output (waits for Node 2 + 3)

Which nodes can run in parallel? Which have dependencies?

## 2. AGENT-PER-NODE DESIGN
For each node, define:
- **Agent role**: One-sentence system prompt
- **Input**: What data it receives from upstream nodes
- **Tools**: What external tools/APIs it can call
- **Output schema**: Structured JSON output format
- **Success criteria**: How to know the node succeeded
- **Fallback**: What happens on failure (retry / skip / escalate)

## 3. STATE MANAGEMENT
```typescript
interface WorkflowState {
  id: string;
  status: "running" | "completed" | "failed";
  nodes: Record<string, {
    status: "pending" | "running" | "completed" | "failed";
    input: any;
    output: any;
    retries: number;
    startedAt?: string;
    completedAt?: string;
  }>;
  context: Record<string, any>; // shared context across nodes
}
```

## 4. ORCHESTRATOR LOGIC
- Event-driven: Each node completion triggers downstream nodes
- Checkpoint & resume: Persist state so workflow survives restarts
- Timeout per node: Kill long-running agents
- Cost budget: Stop workflow if total token spend exceeds limit

## 5. OBSERVABILITY
- Log every agent decision and tool call
- Trace ID for end-to-end debugging
- Dashboard: workflow success rate, avg duration, cost per run

Apply to: [DESCRIBE YOUR WORKFLOW]

## Tips

Agentic workflows are the production pattern for complex multi-step AI processes. Used by LangGraph, CrewAI, and Temporal-based AI systems.
