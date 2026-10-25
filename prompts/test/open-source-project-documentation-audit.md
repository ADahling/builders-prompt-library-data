---
title: "Open Source Project Documentation Audit"
slug: open-source-project-documentation-audit
stage: Test
category: "Quality Audits"
grade: A
score: 81
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/open-source-project-documentation-audit
---
# Open Source Project Documentation Audit

Evaluate open source project documentation for technical accuracy, clarity, and consistency to generate a prioritized improvement roadmap.

Variables: project_name, project_description, target_audience

## Prompt

As a technical writer, I need to conduct a comprehensive audit of the documentation for our open source project, `{{project_name}}`. The project is a {{project_description}}, and the documentation is aimed at {{target_audience}}. We need to ensure our documentation is accurate, complete, and easy to understand.

Your audit should cover the following aspects of our documentation:

1.  **Accuracy and Completeness:**
    *   Review the documentation for technical accuracy and ensure it is up-to-date with the latest version of the project.
    *   Identify any missing information or gaps in the documentation.

2.  **Clarity and Readability:**
    *   Assess the clarity and readability of the documentation. Check for jargon, complex sentences, and other factors that could make the documentation difficult to understand.
    *   Ensure that the documentation is well-structured and easy to navigate.

3.  **Consistency:**
    *   Check for consistency in terminology, formatting, and style across all documentation.

4.  **Examples and Tutorials:**
    *   Review the examples and tutorials to ensure they are clear, accurate, and helpful.
    *   Identify any opportunities to add more examples or tutorials to improve the documentation.

**Output Format:**

Please provide a documentation audit report in a Markdown file with the following structure:

*   **Documentation Quality Score:** A summary of the documentation's overall quality, with scores for each of the audited areas.
*   **Audit Findings:** A detailed list of all identified issues, categorized by the areas mentioned above. For each issue, provide:
    *   **Issue ID:** A unique identifier.
    *   **Severity:** (High, Medium, Low)
    *   **Description:** A clear explanation of the issue.
    *   **Recommendation:** Specific and actionable steps to fix the issue.
*   **Documentation Improvement Plan:** A prioritized list of recommendations for improving the documentation.
