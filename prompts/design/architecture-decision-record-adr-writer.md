---
title: "Architecture Decision Record (ADR) Writer"
slug: architecture-decision-record-adr-writer
stage: Design
category: "Documentation"
grade: A+
score: 94
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/architecture-decision-record-adr-writer
---
# Architecture Decision Record (ADR) Writer

Generate structured Architecture Decision Records to document technical choices, trade-offs, and context for specific project milestones.

Variables: decision_description, project_name, context_1, context_2, number, short_title

## Prompt

You are a software architect. Write an Architecture Decision Record (ADR) for the decision to {{decision_description}} in {{project_name}}.

Context:
- {{context_1}}
- {{context_2}}

Use the standard ADR format:

**Title**: ADR-{{number}}: {{short_title}}

**Status**: Proposed | Accepted | Deprecated | Superseded

**Context**: What is the issue that we're seeing that is motivating this decision or change?

**Decision**: What is the change that we're proposing and/or doing?

**Consequences**: What becomes easier or more difficult to do because of this change?

**Alternatives Considered**: What other options were evaluated?
| Option | Pros | Cons | Effort |

**Decision Drivers**: What factors influenced this decision?

**References**: Links to relevant documentation, discussions, or research.

## Tips

ADRs are the institutional memory of your architecture. Future team members will thank you.
