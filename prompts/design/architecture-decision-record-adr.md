---
title: "Architecture Decision Record (ADR)"
slug: architecture-decision-record-adr
stage: Design
category: "Documentation"
grade: B
score: 78
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/architecture-decision-record-adr
---
# Architecture Decision Record (ADR)

Write a concise architecture decision record documenting context, options, tradeoffs, rationale, consequences, and policy alignment.

## Prompt

Write an Architecture Decision Record for this decision:

Title: [short descriptive title, e.g., "Use PostgreSQL over MongoDB"]
Date: [date]
Status: [proposed / accepted / deprecated / superseded]
Context: [what situation are we in, what forces are at play]

Format:
1. Context: What is the issue that we're seeing that is motivating this decision or change?
2. Decision drivers: What criteria matter most? (performance, cost, team expertise, maintenance, scalability)
3. Considered options:
   - Option A: [description] — pros, cons
   - Option B: [description] — pros, cons
   - Option C: [description] — pros, cons
4. Decision: What is the change that we're proposing and/or doing?
5. Rationale: Why this option over the others? Be specific.
6. Consequences:
   - Positive: What becomes easier?
   - Negative: What becomes harder?
   - Risks: What could go wrong?
7. Compliance: Does this align with existing standards/policies?

Keep it concise. Future-you will thank present-you.

## Tips

ADRs prevent the 'why did we do this?' conversation 6 months later.
