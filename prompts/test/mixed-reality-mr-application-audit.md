---
title: "Mixed Reality (MR) Application Audit"
slug: mixed-reality-mr-application-audit
stage: Test
category: "Quality Audits"
grade: A
score: 88
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/mixed-reality-mr-application-audit
---
# Mixed Reality (MR) Application Audit

Generate a comprehensive UX audit for mixed reality applications to identify usability issues and receive prioritized improvement recommendations.

Variables: application_name, application_description

## Prompt

As a UX designer specializing in MR, I need to conduct a UX audit for our MR application, `{{application_name}}`. The application is a {{application_description}}, and we want to improve the user experience and make the application more intuitive and user-friendly.

Your audit should cover the following aspects of the MR application:

1.  **Onboarding and First-Time User Experience:**
    *   Evaluate the onboarding process for new users.
    *   Ensure that users can easily understand how to use the application.

2.  **Object Tracking and Recognition:**
    *   Assess the accuracy and reliability of the application's object tracking and recognition.

3.  **Interaction Design:**
    *   Review the interaction design of the application.
    *   Ensure that users can easily interact with virtual objects in the real world.

4.  **Performance and Comfort:**
    *   Assess the performance of the application and its impact on user comfort.

**Output Format:**

Please provide a UX audit report in a Markdown file with the a structure:

*   **UX Score:** A summary of the application's overall UX quality, with scores for each of the audited areas.
*   **Audit Findings:** A detailed list of all identified issues, categorized by the areas mentioned above. For each issue, provide:
    *   **Issue ID:** A unique identifier.
    *   **Severity:** (High, Medium, Low)
    *   **Description:** A clear explanation of the issue.
    *   **Recommendation:** Specific and actionable steps to fix the issue.
*   **UX Improvement Plan:** A prioritized list of recommendations for improving the application's UX.
