---
title: "Create a Security Policy and Reporting Guidelines"
slug: create-a-security-policy-and-reporting-guidelines
stage: Design
category: "Documentation"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-security-policy-and-reporting-guidelines
---
# Create a Security Policy and Reporting Guidelines

Draft a Markdown security policy for an open-source project, with supported versions and private vulnerability reporting via GitHub and email.

Variables: project_name, project_domain

## Prompt

To ensure that security vulnerabilities in my open-source project, `{{project_name}}`, are handled responsibly, I need to create a `SECURITY.md` file. This file will outline the project's security policy and provide clear instructions for how to privately report a vulnerability.

Generate a complete `SECURITY.md` file in Markdown format. The file should be based on GitHub's recommended template and include the following sections:

1.  **Supported Versions**: A table indicating which versions of the project are currently supported with security updates. This helps users understand if they need to upgrade.
    *   Example:
        | Version | Supported          |
        | ------- | ------------------ |
        | 5.1.x   | :white_check_mark: |
        | 5.0.x   | :x:                |
        | 4.0.x   | :white_check_mark: |

2.  **Reporting a Vulnerability**: This is the most critical section. It must provide clear, step-by-step instructions for how to report a security vulnerability privately.
    *   State clearly that security issues should NOT be reported in public GitHub issues.
    *   Provide the primary method for reporting. The best practice is to enable private vulnerability reporting on GitHub. Instruct users to go to the "Security" tab of the repository and click "Report a vulnerability".
    *   Provide a secondary, email-based method as a backup (e.g., `security@{{project_domain}}.com`).
    *   Describe the information that should be included in the report (e.g., detailed description, potential impact, reproduction steps).
    *   Set expectations for the response time (e.g., "You should receive an initial response within 48 hours.").

3.  **Security Disclosure Process**: Briefly explain what will happen after a vulnerability is reported and confirmed. Mention that the project team will coordinate with the reporter and set a timeline for releasing a patch and a public advisory.

Your output should be a complete Markdown file, ready to be committed to the repository's root or `.github` directory.

Constraint Checklist & Confidence Score:
1.  Does the file clearly explain how to report a vulnerability privately? Yes.
2.  Does it follow the standard structure for a SECURITY.md file? Yes.
3.  Does it set clear expectations for reporters? Yes.
4.  Is the information about supported versions clear? Yes.

Confidence Score: 5/5

Strategizing complete. I will now generate the SECURITY.md file content.

## Tips

A SECURITY.md file is a critical part of responsible open-source maintenance. It protects your users by ensuring vulnerabilities are disclosed safely.
