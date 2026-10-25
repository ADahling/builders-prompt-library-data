---
title: "HIPAA Compliance Checklist for a Mobile Health App"
slug: hipaa-compliance-checklist-for-a-mobile-health-app
stage: Secure
category: "Security Review"
grade: A+
score: 95
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/hipaa-compliance-checklist-for-a-mobile-health-app
---
# HIPAA Compliance Checklist for a Mobile Health App

Generate a structured HIPAA compliance checklist across the Privacy, Security, and Breach Notification Rules for a mobile health application.

Variables: app_name, tech_stack

## Prompt

You are a healthcare compliance consultant. A startup has developed a new mobile health application, {{app_name}}, that allows users to track their symptoms and share the data with their doctors. The app is built using {{tech_stack}}. The startup needs to ensure their app is HIPAA compliant.

Create a detailed HIPAA compliance checklist for the development team. The checklist should be in Markdown format and cover the three main HIPAA rules: the Privacy Rule, the Security Rule, and the Breach Notification Rule.

For each item on the checklist, provide:

*   **Control:** A clear and concise description of the requirement.
*   **Explanation:** A brief explanation of why this is important for HIPAA compliance.
*   **Implementation Guidance:** Actionable advice on how to implement the control in the context of a mobile health app.

Your checklist should be comprehensive and cover topics such as:

*   **Privacy Rule:**
    *   Notice of Privacy Practices
    *   Minimum Necessary Use
    *   Individual Rights (Access, Amendment, etc.)
*   **Security Rule:**
    *   **Administrative Safeguards:** Security management process, assigned security responsibility, workforce security, etc.
    *   **Physical Safeguards:** Facility access controls, workstation security, etc. (as applicable to their cloud provider).
    *   **Technical Safeguards:** Access control, audit controls, integrity, transmission security.
*   **Breach Notification Rule:**
    *   Breach definition
    *   Notification requirements to individuals, the HHS Secretary, and the media.

Your output should be a practical and easy-to-use checklist that the startup can use to guide their compliance efforts.
