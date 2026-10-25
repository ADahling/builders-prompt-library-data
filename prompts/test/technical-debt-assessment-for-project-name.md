---
title: "Technical Debt Assessment for {{project_name}}"
slug: technical-debt-assessment-for-project-name
stage: Test
category: "Quality Audits"
grade: A
score: 87
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/technical-debt-assessment-for-project-name
---
# Technical Debt Assessment for {{project_name}}

Get a Markdown technical debt assessment covering code, architecture, tests, and development processes for a project with accumulated debt.

Variables: project_name, project_description, development_duration

## Prompt

As a senior engineering manager, I need a comprehensive technical debt assessment for our project, `{{project_name}}`. The project is a {{project_description}} and has been in development for {{development_duration}}. We need to understand the extent of our technical debt and create a plan for managing and reducing it.

Your assessment should be a deep dive into our codebase and development processes to identify and quantify our technical debt. The assessment should cover the following areas:

1.  **Code-Level Debt:**
    *   Analyze the codebase for code smells, anti-patterns, and other indicators of technical debt.
    *   Use static analysis tools to measure metrics such as cyclomatic complexity, code duplication, and code coverage.

2.  **Architectural Debt:**
    *   Review the system architecture for any design flaws or outdated patterns that are contributing to technical debt.
    *   Assess the modularity and coupling of the system.

3.  **Test Debt:**
    *   Analyze the test suite for any gaps in coverage or low-quality tests.
    *   Identify any areas of the codebase that are difficult to test.

4.  **Process Debt:**
    *   Review our development processes for any inefficiencies or bottlenecks that are contributing to the accumulation of technical debt.

**Output Format:**

Please provide a technical debt assessment report in a Markdown file with the following structure:

*   **Technical Debt Quadrant:** A visualization of our technical debt, categorized by type (e.g., reckless vs. prudent, deliberate vs. inadvertent).
*   **Technical Debt Register:** A detailed list of all identified technical debt items. For each item, provide:
    *   **Debt ID:** A unique identifier.
    *   **Description:** A clear explanation of the technical debt item.
    *   **Impact:** The impact of the technical debt on the project (e.g., increased development time, higher bug rate).
    *   **Repayment Cost:** An estimate of the effort required to repay the technical debt.
*   **Technical Debt Reduction Plan:** A prioritized plan for repaying our technical debt. The plan should include specific actions, timelines, and owners.
