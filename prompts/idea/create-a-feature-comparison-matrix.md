---
title: "Create a Feature Comparison Matrix"
slug: create-a-feature-comparison-matrix
stage: Idea
category: "Business & Strategy"
grade: A+
score: 96
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-feature-comparison-matrix
---
# Create a Feature Comparison Matrix

Generate a detailed markdown matrix and competitive analysis to identify feature gaps and market differentiators against key rivals.

Variables: tool_name, competitor_A, competitor_B, competitor_C

## Prompt

I am the lead developer for a new project management tool, {{tool_name}}. We are entering a crowded market and need to understand how our feature set compares to the competition. Our main competitors are {{competitor_A}}, {{competitor_B}}, and {{competitor_C}}.

I need you to generate a feature comparison matrix. You should act as a product analyst and research the features of each competitor. The matrix should compare the following features:

*   Task Management (e.g., subtasks, dependencies, custom fields)
*   Collaboration (e.g., real-time editing, comments, @mentions)
*   Views (e.g., Kanban, Gantt, Calendar)
*   Integrations (e.g., Slack, Google Drive, GitHub)
*   Reporting & Analytics
*   Mobile App Availability (iOS & Android)
*   Security & Compliance (e.g., SOC 2, GDPR)

**Output Format:**

Please create a Markdown table with the features as rows and the competitors (including our product, {{tool_name}}) as columns. Use the following symbols to indicate feature availability:

*   ✅: Full support
*   🟡: Partial support or requires a paid add-on
*   ❌: Not supported

After the matrix, provide a brief analysis of the key takeaways. Highlight the features that are table stakes in this market, and identify any features that could be a key differentiator for {{tool_name}}.

**Constraints:**

*   The information should be as accurate as possible based on the competitors' websites and documentation.
*   The output should be a clean, easy-to-read Markdown table.

## Tips

A great prompt for getting a quick, high-level overview of the feature landscape in a specific market.
