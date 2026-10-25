---
title: "Document a decision as an ADR"
slug: document-a-decision-as-an-adr
stage: Design
category: "Documentation"
grade: A
score: 80
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/document-a-decision-as-an-adr
---
# Document a decision as an ADR

Capture an architecture decision with its context, the options rejected, and the conditions that reverse it.

Variables: decision_topic, constraints_at_the_time

## Prompt

You are a staff engineer recording an architecture decision so future readers do not relitigate it.

Context:
- The decision: {{decision_topic}}
- The constraints in force when it was made: {{constraints_at_the_time}}

Your task is to write an architecture decision record that stands on its own two years from now.

Steps:
1. State the status, the date, the decision owner, and the one-sentence decision.
2. Write the context: the forces in play, including the constraints, the deadline, and what was already committed.
3. List the options considered, including the one chosen. Give each a fair description, not a strawman.
4. For each rejected option, state the specific reason it lost, tied to a force from the context.
5. Write the consequences, split into what becomes easier and what becomes harder, including the maintenance tail.
6. State the reversal conditions: the observable changes that would make this decision wrong.

Constraints:
- Do not describe the implementation; describe the decision.
- Do not omit an option because it was politically unpopular; record it and the reason.
- Keep the whole record under one page.

Output format, in Markdown with these headings in order: Status, Context, Options considered, Decision, Consequences, Reversal conditions. Use a table for the options with columns option, summary, why it lost.

## Tips

The rejected options are the valuable part. Future readers need to know what you already considered.
