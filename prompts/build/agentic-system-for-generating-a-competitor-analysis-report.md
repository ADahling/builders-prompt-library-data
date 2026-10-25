---
title: "Agentic System for Generating a Competitor Analysis Report"
slug: agentic-system-for-generating-a-competitor-analysis-report
stage: Build
category: "AI Agent Development"
grade: B
score: 79
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/agentic-system-for-generating-a-competitor-analysis-report
---
# Agentic System for Generating a Competitor Analysis Report

Get a Python agent pipeline that researches a competitor and produces a Markdown report on features, pricing, marketing, and differentiation.

Variables: competitor_name, our_company_name

## Prompt

Design a multi-agent system that performs a competitor analysis and generates a report.

**The Goal:**

Analyze the company `{{competitor_name}}` and compare it to our company, `{{our_company_name}}`.

**The Agent Crew:**

1.  **Web Presence Agent:**
    *   **Task:** Use a web search tool to find the competitor's website, blog, and social media profiles.
2.  **Product Feature Agent:**
    *   **Task:** Analyze the competitor's website to identify their key product features and pricing.
3.  **Marketing Angle Agent:**
    *   **Task:** Analyze the competitor's blog and social media to understand their marketing angle and target audience.
4.  **Synthesis Agent:**
    *   **Task:** Combine all the gathered information into a report that summarizes the competitor's strategy and suggests 2-3 ways our company can differentiate itself.

**The Orchestration:**

Write a Python script that runs this four-agent pipeline.

**Output:**

A Python script that generates the competitor analysis report in a structured Markdown file.
