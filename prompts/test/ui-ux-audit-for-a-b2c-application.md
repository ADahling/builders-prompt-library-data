---
title: "UI/UX Audit for a B2C Application"
slug: ui-ux-audit-for-a-b2c-application
stage: Test
category: "Quality Audits"
grade: A
score: 87
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/ui-ux-audit-for-a-b2c-application
---
# UI/UX Audit for a B2C Application

Perform a comprehensive heuristic evaluation and UI/UX audit to identify usability gaps and generate a prioritized improvement roadmap.

Variables: project_name, project_description, target_audience

## Prompt

As a UI/UX designer, I need to conduct a UI/UX audit for our B2C application, `{{project_name}}`. This application is a {{project_description}} and we want to improve the user experience and make the application more intuitive and user-friendly. The target audience is {{target_audience}}.

Your audit should be based on a heuristic evaluation using Jakob Nielsen's 10 usability heuristics. For each heuristic, please evaluate the application and provide a score from 1 to 5 (1 = major usability issue, 5 = no usability issues). In addition to the heuristic evaluation, your audit should also cover:

1.  **Visual Design and Branding:**
    *   Assess the consistency of the visual design, including colors, typography, and iconography.
    *   Evaluate how well the design reflects our brand identity.

2.  **Information Architecture and Navigation:**
    *   Analyze the information architecture and navigation to ensure that users can easily find what they are looking for.
    *   Identify any usability issues with the navigation menus, breadcrumbs, and search functionality.

3.  **Forms and Input:**
    *   Review the design of all forms to ensure they are easy to use and understand.
    *   Check for clear error messaging and input validation.

4.  **Onboarding and User Guidance:**
    *   Evaluate the user onboarding process and identify any areas for improvement.
    *   Assess the effectiveness of any in-app guidance, such as tooltips and tutorials.

**Output Format:**

Please provide a UI/UX audit report in a Markdown file with the following structure:

*   **Overall Usability Score:** An average score based on the heuristic evaluation.
*   **Heuristic Evaluation:** A detailed breakdown of the heuristic evaluation, with a score and comments for each heuristic.
*   **UI/UX Issues and Recommendations:** A prioritized list of all identified UI/UX issues. For each issue, provide:
    *   **Issue ID:** A unique identifier.
    *   **Severity:** (High, Medium, Low)
    *   **Description:** A clear explanation of the issue, with screenshots to illustrate the problem.
    *   **Recommendation:** A specific and actionable recommendation for fixing the issue, with mockups or wireframes if necessary.
*   **UI/UX Improvement Plan:** A high-level plan for improving the UI/UX of the application.

Your report should provide our team with a clear understanding of the usability issues in our application and a roadmap for addressing them.
