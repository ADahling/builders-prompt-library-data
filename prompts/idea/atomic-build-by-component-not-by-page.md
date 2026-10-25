---
title: "ATOMIC \u2014 Build by Component, Not by Page"
slug: atomic-build-by-component-not-by-page
stage: Idea
category: "Prompt Engineering"
grade: C
score: 63
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/atomic-build-by-component-not-by-page
---
# ATOMIC — Build by Component, Not by Page

Build a feature one component at a time with typed props, mock data, and all UI states, requiring approval before connecting components.

## Prompt

Build this feature one small, isolated component at a time. Do NOT generate an entire page or multiple components at once.

For each component:
1. Build ONLY that component with its props, types, and internal logic.
2. Show me the component in isolation before connecting it to anything else.
3. Include TypeScript types for all props.
4. Handle all states: loading, error, empty, and populated.
5. Make it work with mock data first.

Only after I approve each component should you wire them together into the full page.

Start with the smallest, most reusable piece first.

## Tips

From Reddit r/lovable — prevents the AI from generating huge, tangled components. Smaller = fewer bugs. Source: reddit.com/r/lovable/comments/1px6vpg
