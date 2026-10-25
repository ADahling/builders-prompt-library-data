---
title: "Component Extraction from a Marketing Site"
slug: component-extraction-from-a-marketing-site
stage: Build
category: "Website Cloning"
grade: C
score: 65
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/component-extraction-from-a-marketing-site
---
# Component Extraction from a Marketing Site

Reconstruct a tiered pricing table from a marketing URL into a reusable, framework-agnostic component with structured props.

Variables: marketing_site_url

## Prompt

You are a mid-level front-end engineer. Your task is to extract a reusable 'pricing table' component from a marketing website and rebuild it as a standalone component.

Context:
- The target website is {{marketing_site_url}}.
- The pricing table has multiple tiers and a feature comparison list.
- You should use a modern JavaScript framework like React or Vue to create the component.

Provide:
1. The code for the reusable pricing table component.
2. A brief explanation of the component's props and how to use it.

If you cannot open {{marketing_site_url}} yourself, say so before anything else and ask me for screenshots at each breakpoint or the page's HTML and CSS. Do not invent the design or describe it as verified.
If the full result does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue.

## Tips

This task helps practice component-based architecture and code organization.
