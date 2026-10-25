---
title: "Create an Issue Template for Bug Reports"
slug: create-an-issue-template-for-bug-reports
stage: Test
category: "Testing & QA"
grade: A+
score: 99
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-an-issue-template-for-bug-reports
---
# Create an Issue Template for Bug Reports

Draft a GitHub bug report template for an open-source project with YAML metadata, reproduction steps, and environment details.

Variables: project_name

## Prompt

Generate a comprehensive bug report issue template for an open-source project named `{{project_name}}`. The template should be in Markdown format and saved as `.github/ISSUE_TEMPLATE/bug_report.md`. The goal is to standardize bug reporting and ensure that maintainers receive all the necessary information to diagnose and fix issues efficiently.

The template should have a clear structure and prompt the user to provide specific details. It should include:

1.  **Template Configuration** (YAML front matter):
    *   `name`: Bug Report
    *   `about`: Create a report to help us improve
    *   `title`: "[BUG] - "
    *   `labels`: ["bug", "triage"]
    *   `assignees`: ''

2.  **Template Body** (Markdown):
    *   **Describe the bug**: A clear and concise description of what the bug is.
    *   **To Reproduce**: Steps to reproduce the behavior. Be very specific.
        ```
        1. Go to '...'
        2. Click on '....'
        3. Scroll down to '....'
        4. See error
        ```
    *   **Expected behavior**: A clear and concise description of what you expected to happen.
    *   **Screenshots**: If applicable, add screenshots to help explain your problem.
    *   **Desktop Environment (please complete the following information):**
        *   OS: [e.g. iOS]
        *   Browser [e.g. chrome, safari]
        *   Version [e.g. 22]
    *   **Smartphone (please complete the following information):**
        *   Device: [e.g. iPhone6]
        *   OS: [e.g. iOS8.1]
        *   Browser [e.g. stock browser, safari]
        *   Version [e.g. 22]
    *   **Additional context**: Add any other context about the problem here.

Your output should be the complete content for the `bug_report.md` file, including the YAML front matter.

Constraint Checklist & Confidence Score:
1.  Is the template in valid Markdown format with YAML front matter? Yes.
2.  Does it prompt for all necessary information (description, reproduction steps, environment)? Yes.
3.  Is the structure clear and easy for a user to fill out? Yes.
4.  Are the default labels and title appropriate for a bug report? Yes.

Confidence Score: 5/5

Strategizing complete. I will now generate the bug report issue template file content.

## Tips

Standardized issue templates are essential for managing incoming bug reports and feature requests in a structured way.
