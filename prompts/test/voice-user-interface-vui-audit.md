---
title: "Voice User Interface (VUI) Audit"
slug: voice-user-interface-vui-audit
stage: Test
category: "Quality Audits"
grade: A
score: 80
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/voice-user-interface-vui-audit
---
# Voice User Interface (VUI) Audit

Evaluate a voice application's natural language, error handling, and intent recognition to produce a prioritized UX improvement report.

Variables: application_name, application_description

## Prompt

As a VUI designer, I need to conduct a VUI audit for our voice application, `{{application_name}}`. The application is a {{application_description}}, and we want to improve the user experience and make the application more intuitive and user-friendly.

Your audit should cover the following aspects of the VUI:

1.  **Clarity and Natural Language:**
    *   Assess the clarity and natural language of the application's responses.
    *   Check for jargon, complex sentences, and other factors that could make the application difficult to understand.

2.  **Error Handling and Fallbacks:**
    *   Review the application's error handling and fallback mechanisms.
    *   Ensure that the application can gracefully handle unexpected user input.

3.  **User Intent Recognition:**
    *   Assess the application's ability to understand user intent.
    *   Identify any common user intents that the application is not able to handle.

4.  **Personalization and Context:**
    *   Review the application's use of personalization and context.
    *   Ensure that the application can remember previous user interactions and provide a personalized experience.

**Output Format:**

Please provide a VUI audit report in a Markdown file with the following structure:

*   **VUI Score:** A summary of the application's overall VUI quality, with scores for each of the audited areas.
*   **Audit Findings:** A detailed list of all identified issues, categorized by the areas mentioned above. For each issue, provide:
    *   **Issue ID:** A unique identifier.
    *   **Severity:** (High, Medium, Low)
    *   **Description:** A clear explanation of the issue.
    *   **Recommendation:** Specific and actionable steps to fix the issue.
*   **VUI Improvement Plan:** A prioritized list of recommendations for improving the application's VUI.
