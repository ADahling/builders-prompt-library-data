---
title: "OpenClaw: Architecture Decision Records (ADRs)"
slug: openclaw-architecture-decision-records-adrs
stage: Build
category: "OpenClaw"
grade: A+
score: 92
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-architecture-decision-records-adrs
---
# OpenClaw: Architecture Decision Records (ADRs)

Draft and save an architecture decision record for a technical change with context, alternatives, tradeoffs, risks, and follow-up actions.

Variables: title-slug, number, Title, YYYY-MM-DD, Proposed / Accepted / Deprecated / Superseded by ADR-XX, Names/roles, What is the issue that we're seeing that is motivating this decision or change?, Include relevant metrics, constraints, and business requirements., What is the change that we're proposing and/or doing?, Be specific about technologies, patterns, or approaches chosen., Name, list, estimate, Expected benefits, Known tradeoffs and technical debt incurred, What could go wrong and mitigation strategies, Specific task 1, Specific task 2, timeframe

## Prompt

# Architecture Decision Record Generator — OpenClaw Workflow Prompt

## Trigger
Activate when asked to document a technical decision or when significant architectural changes are discussed.

## ADR Template
Generate an ADR in this format and save to docs/decisions/YYYY-MM-DD-{{title-slug}}.md:

```markdown
# ADR-{{number}}: {{Title}}

**Date:** {{YYYY-MM-DD}}
**Status:** {{Proposed / Accepted / Deprecated / Superseded by ADR-XX}}
**Decision Makers:** {{Names/roles}}

## Context
{{What is the issue that we're seeing that is motivating this decision or change?}}
{{Include relevant metrics, constraints, and business requirements.}}

## Decision
{{What is the change that we're proposing and/or doing?}}
{{Be specific about technologies, patterns, or approaches chosen.}}

## Alternatives Considered

### Option A: {{Name}}
- **Pros:** {{list}}
- **Cons:** {{list}}
- **Effort:** {{estimate}}

### Option B: {{Name}} ← Selected
- **Pros:** {{list}}
- **Cons:** {{list}}
- **Effort:** {{estimate}}

### Option C: {{Name}}
- **Pros:** {{list}}
- **Cons:** {{list}}
- **Effort:** {{estimate}}

## Consequences
### Positive
- {{Expected benefits}}

### Negative
- {{Known tradeoffs and technical debt incurred}}

### Risks
- {{What could go wrong and mitigation strategies}}

## Follow-Up Actions
- [ ] {{Specific task 1}}
- [ ] {{Specific task 2}}
- [ ] Review in {{timeframe}} to validate decision
```

## Agent Behavior
- When a technical debate happens in Slack/chat, proactively suggest creating an ADR
- Maintain an index of all ADRs in docs/decisions/README.md
- Link related ADRs together (superseded, related)
- Flag when an ADR is >6 months old and hasn't been reviewed

## Tips

Generates Architecture Decision Records from technical discussions. Proactively suggests documentation when debates happen. From Rezvani's developer automation prompts.
