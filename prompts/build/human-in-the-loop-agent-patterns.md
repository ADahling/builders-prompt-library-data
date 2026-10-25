---
title: "Human-in-the-Loop Agent Patterns"
slug: human-in-the-loop-agent-patterns
stage: Build
category: "AI Agent Development"
grade: A
score: 82
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/human-in-the-loop-agent-patterns
---
# Human-in-the-Loop Agent Patterns

Design human oversight for an AI agent with confidence-based routing, approval gates, correction feedback, escalation protocols, and approval UI.

## Prompt

Design a human-in-the-loop (HITL) system for an AI agent that handles [describe task]:

## 1. CONFIDENCE-BASED ROUTING
```
Agent processes request → Confidence score?
  - HIGH (>0.9): Auto-execute, log for audit
  - MEDIUM (0.6-0.9): Execute but flag for review
  - LOW (<0.6): Pause and ask human for guidance
```

## 2. APPROVAL GATES
Define which actions ALWAYS require human approval:
- Destructive operations (delete, overwrite, send)
- Financial transactions above threshold
- External API calls with side effects
- Actions affecting other users

```typescript
interface ApprovalRequest {
  action: string;
  reasoning: string; // why the agent wants to do this
  impact: "low" | "medium" | "high";
  alternatives: string[]; // other options the agent considered
  timeoutAction: "cancel" | "proceed-with-default";
  timeoutMinutes: number;
}
```

## 3. FEEDBACK LOOP
When a human corrects the agent:
- Store the correction as a training example
- Update agent's system prompt or few-shot examples
- Track correction patterns to identify systematic errors
- Gradually reduce HITL as agent accuracy improves

## 4. ESCALATION PROTOCOL
- Level 1: Agent retries with different approach
- Level 2: Agent asks user for clarification
- Level 3: Agent hands off to human with full context summary
- Level 4: Alert on-call team (for production agents)

## 5. UX DESIGN
- Approval UI: Show what the agent wants to do + why
- Batch approvals: Group similar low-risk actions
- Async approvals: Queue actions for later review
- Mobile notifications for time-sensitive approvals

Apply to: [DESCRIBE YOUR AGENT AND ITS RISK PROFILE]

## Tips

Pure autonomy is rarely the goal. The best production agents know when to ask for help. Used by Devin, Cursor, and enterprise AI workflows.
