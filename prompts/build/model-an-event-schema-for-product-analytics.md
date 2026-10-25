---
title: "Model an event schema for product analytics"
slug: model-an-event-schema-for-product-analytics
stage: Build
category: "Modern Data Stack"
grade: A
score: 82
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/model-an-event-schema-for-product-analytics
---
# Model an event schema for product analytics

Design a versioned event taxonomy with stable names, typed properties, and an evolution policy.

Variables: product_area, key_questions

## Prompt

You are a data engineer designing the event schema for a product area.

Context:
- The product area: {{product_area}}
- The questions the data must answer: {{key_questions}}

Your task is to define an event taxonomy that answers those questions and survives two years of product change.

Steps:
1. Work backwards from each question to the minimum events and properties that answer it. Drop anything no question needs.
2. Define the naming convention: object then past-tense action, lower snake case, with the rule written out and three examples.
3. Specify each event: name, when it fires, the properties with types and nullability, and the identity fields attached.
4. Define the shared context sent with every event, including schema version, and state what must never be included.
5. Write the evolution policy: how a property is added, deprecated, and removed, and what breaks a consumer.
6. Define the validation step in the pipeline that rejects malformed events, and where rejects land.

Constraints:
- No personally identifying data in event properties; use identifiers that resolve elsewhere.
- No event named after a UI component or a code path.
- Every event must be traceable to at least one of the stated questions.

Output format, in Markdown: a question-to-event mapping table, one section per event with a JSON example in a fenced block, then **Shared context**, **Evolution policy**, and **Validation** as sections.

## Tips

Name events after what the user did, not what the code did. Implementation names rot at the first refactor.
