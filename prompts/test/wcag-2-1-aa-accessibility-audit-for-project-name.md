---
title: "WCAG 2.1 AA Accessibility Audit"
slug: wcag-2-1-aa-accessibility-audit-for-project-name
stage: Test
category: "Quality Audits"
grade: A
score: 84
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/wcag-2-1-aa-accessibility-audit-for-project-name
---
# WCAG 2.1 AA Accessibility Audit

Get a Markdown WCAG 2.1 AA audit report identifying website accessibility issues and recommending fixes across the four core principles.

Variables: project_name, project_description, tech_stack

## Prompt

As a front-end developer, I need to conduct an accessibility audit for our website, `{{project_name}}`, to ensure it complies with the Web Content Accessibility Guidelines (WCAG) 2.1 Level AA. The website is a {{project_description}} built with {{tech_stack}}.

Your task is to perform a detailed audit of the website and provide a report that identifies all accessibility issues and provides clear recommendations for fixing them. The audit should cover the following aspects of accessibility:

1.  **Perceivable:**
    *   Provide text alternatives for all non-text content.
    *   Ensure that all content is available to users with visual impairments (e.g., through screen readers).
    *   Check for sufficient color contrast between text and background.

2.  **Operable:**
    *   Ensure that all functionality is available from a keyboard.
    *   Provide mechanisms to help users navigate, find content, and determine where they are.
    *   Avoid content that could cause seizures.

3.  **Understandable:**
    *   Make text content readable and understandable.
    *   Make web pages appear and operate in predictable ways.
    *   Help users avoid and correct mistakes.

4.  **Robust:**
    *   Maximize compatibility with current and future user agents, including assistive technologies.

**Output Format:**

Please provide an accessibility audit report in a Markdown file with the following structure:

*   **Summary of Findings:** A high-level overview of the website's accessibility and a summary of the most critical issues found.
*   **Accessibility Issues:** A detailed list of all identified accessibility issues, categorized by the four principles of accessibility (Perceivable, Operable, Understandable, and Robust). For each issue, provide:
    *   **Issue ID:** A unique identifier.
    *   **WCAG Guideline:** The specific WCAG guideline that is violated.
    *   **Description:** A clear explanation of the issue and its impact on users with disabilities.
    *   **Location:** The URL and a screenshot of where the issue occurs.
    *   **Remediation:** Specific and actionable steps to fix the issue, including code examples where appropriate.
*   **Recommendations:** A list of recommendations for improving the overall accessibility of the website.

Your report should be comprehensive and provide our team with a clear path to achieving WCAG 2.1 AA compliance.
