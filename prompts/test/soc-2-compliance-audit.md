---
title: "SOC 2 Compliance Audit"
slug: soc-2-compliance-audit
stage: Test
category: "Quality Audits"
grade: C
score: 69
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/soc-2-compliance-audit
---
# SOC 2 Compliance Audit

Conduct a comprehensive SOC 2 audit to identify security gaps and generate a prioritized remediation roadmap for regulatory compliance.

Variables: project_name, project_description

## Prompt

As a compliance officer, I need you to perform a compliance audit of our application, `{{project_name}}`, against the SOC 2 standard. The application is a {{project_description}} and handles sensitive customer data. We need to ensure that our application and processes are fully compliant with the requirements of SOC 2.

Your audit should be a comprehensive assessment of our compliance posture, covering all relevant aspects of the SOC 2. This includes, but is not limited to:

1.  **Security:**
    *   Review our security controls to ensure they meet the requirements of SOC 2.
    *   This includes reviewing our network security, application security, and physical security controls.

2.  **Availability:**
    *   Assess our systems to ensure they are available for operation and use as committed or agreed.

3.  **Processing Integrity:**
    *   Review our system processing to ensure it is complete, valid, accurate, timely, and authorized.

4.  **Confidentiality:**
    *   Assess our controls to ensure that confidential information is protected as committed or agreed.

5.  **Privacy:**
    *   Review our controls to ensure that personal information is collected, used, retained, disclosed, and disposed of in conformity with the commitments in the entity's privacy notice.

**Output Format:**

Please provide a compliance audit report in a Markdown file with the following structure:

*   **Compliance Status:** A high-level overview of our compliance status, with a clear statement on whether we are compliant with SOC 2.
*   **Audit Findings:** A detailed list of all identified compliance gaps and areas of non-compliance. For each finding, provide:
    *   **Finding ID:** A unique identifier.
    *   **Requirement:** The specific requirement of SOC 2 that is not being met.
    *   **Description:** A clear explanation of the compliance gap.
    *   **Risk:** The potential risk to our organization as a result of the compliance gap.
    *   **Recommendation:** Specific and actionable steps to address the compliance gap.
*   **Compliance Roadmap:** A prioritized plan for achieving full compliance with SOC 2.
