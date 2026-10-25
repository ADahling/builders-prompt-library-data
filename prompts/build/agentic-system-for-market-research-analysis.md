---
title: "Agentic System for Market Research Analysis"
slug: agentic-system-for-market-research-analysis
stage: Build
category: "AI Agent Development"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/agentic-system-for-market-research-analysis
---
# Agentic System for Market Research Analysis

Get a Python agent pipeline that generates a Markdown market report with competitor SWOT analyses and positioning for a new product idea.

Variables: product_idea

## Prompt

Design a multi-agent system that performs a basic market research analysis for a new product idea.

**The Goal:**

Analyze the market viability of a `{{product_idea}}`.

**The Agent Crew:**

1.  **Competitor Analysis Agent:**
    *   **Task:** Use a web search tool to identify the top 3-5 competitors for the given product idea.
2.  **SWOT Analysis Agent:**
    *   **Task:** For each competitor, perform a brief SWOT analysis (Strengths, Weaknesses, Opportunities, Threats).
3.  **Market Positioning Agent:**
    *   **Task:** Based on the competitor analysis, suggest a unique value proposition and a target market segment for the new product idea.
4.  **Synthesis Agent:**
    *   **Task:** Combine all the information into a final, concise market research report.

**The Orchestration:**

Write a Python script that runs this four-agent pipeline. The final output should be a structured report.

**Output:**

A Python script that generates the market research report in Markdown format, with clear sections for each part of the analysis.
