---
title: "Application Compliance Audit"
slug: compliance-audit-for-project-name-against-compliance-standard
stage: Test
category: "Quality Audits"
grade: A
score: 87
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/compliance-audit-for-project-name-against-compliance-standard
---
# Application Compliance Audit

Audit a sensitive-data application's privacy, security controls, policies, and employee training against a specified compliance standard.

Variables: project_name, compliance_standard, project_description

## Prompt

As a compliance officer, I need you to perform a compliance audit of our application, `{{project_name}}`, against the {{compliance_standard}} standard (e.g., GDPR, HIPAA, PCI DSS). The application is a {{project_description}} and handles sensitive data. We need to ensure that our application and processes are fully compliant with the requirements of {{compliance_standard}}.

Your audit should be a comprehensive assessment of our compliance posture, covering all relevant aspects of the {{compliance_standard}}. This includes, but is not limited to:

1.  **Data Protection and Privacy:**
    *   Review our data handling processes to ensure that we are collecting, processing, and storing data in a compliant manner.
    *   Assess the implementation of data protection controls, such as encryption and access control.

2.  **Security Controls:**
    *   Audit our security controls to ensure they meet the requirements of {{compliance_standard}}.
    *   This includes reviewing our network security, application security, and physical security controls.

3.  **Policies and Procedures:**
    *   Review our policies and procedures to ensure they are aligned with the requirements of {{compliance_standard}}.
    *   This includes our incident response plan, data breach notification procedure, and other relevant policies.

4.  **Training and Awareness:**
    *   Assess our employee training and awareness program to ensure that all employees are aware of their responsibilities under {{compliance_standard}}.

**Output Format:**

Please provide a compliance audit report in a Markdown file with the following structure:

*   **Compliance Status:** A high-level overview of our compliance status, with a clear statement on whether we are compliant with {{compliance_standard}}.
*   **Audit Findings:** A detailed list of all identified compliance gaps and areas of non-compliance. For each finding, provide:
    *   **Finding ID:** A unique identifier.
    *   **Requirement:** The specific requirement of {{compliance_standard}} that is not being met.
    *   **Description:** A clear explanation of the compliance gap.
    *   **Risk:** The potential risk to our organization as a result of the compliance gap.
    *   **Recommendation:** Specific and actionable steps to address the compliance gap.
*   **Compliance Roadmap:** A prioritized plan for achieving full compliance with {{compliance_standard}}.
