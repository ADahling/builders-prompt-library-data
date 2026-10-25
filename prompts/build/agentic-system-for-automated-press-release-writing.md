---
title: "Agentic System for Automated Press Release Writing"
slug: agentic-system-for-automated-press-release-writing
stage: Build
category: "AI Agent Development"
grade: B
score: 79
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/agentic-system-for-automated-press-release-writing
---
# Agentic System for Automated Press Release Writing

Get a four-agent Python pipeline that writes headlines, body copy, and boilerplate for a company announcement press release.

Variables: company_name, announcement, ceo_name

## Prompt

Design a multi-agent system that writes a press release for a company announcement.

**The Goal:**

Write a press release about `{{company_name}}` announcing `{{announcement}}` (e.g., "a new product launch", "a major funding round").

**The Agent Crew:**

1.  **Headline Writer Agent:**
    *   **Task:** Brainstorm 5 catchy, professional headlines for the press release.
2.  **Boilerplate Agent:**
    *   **Task:** Write the standard "About {{company_name}}" boilerplate paragraph that goes at the end of a press release.
3.  **Body Writer Agent:**
    *   **Task:** Take the best headline and the core announcement details and write the full body of the press release, including a quote from the CEO, `{{ceo_name}}`.
4.  **Finalizer Agent:**
    *   **Task:** Assemble the headline, body, and boilerplate into a single, properly formatted press release document.

**The Orchestration:**

Write a Python script that runs this four-agent pipeline.

**Output:**

A Python script that outputs the final press release in a text file.
