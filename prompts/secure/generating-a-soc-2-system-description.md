---
title: "Generating a SOC 2 System Description"
slug: generating-a-soc-2-system-description
stage: Secure
category: "Security Review"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/generating-a-soc-2-system-description
---
# Generating a SOC 2 System Description

Generate a professional, audit-ready SOC 2 System Description covering company overview, infrastructure, data, and security controls.

Variables: company_name, platform_name, platform_functionality, cloud_provider

## Prompt

You are a senior technical writer preparing a company, {{company_name}}, for its first SOC 2 Type 1 audit. You need to write the System Description section of the SOC 2 report. The system to be described is a SaaS platform, {{platform_name}}, which provides {{platform_functionality}}.

Your task is to generate a comprehensive System Description that is clear, accurate, and provides the auditor with a thorough understanding of the system and the controls in place. The description should be written in a professional tone and formatted in Markdown.

The System Description must include the following sections:

1.  **Company Overview:** A brief introduction to {{company_name}} and its business.
2.  **System Overview:** A high-level description of the {{platform_name}} platform, its key features, and the services it provides to customers.
3.  **System Components:** A detailed description of the key components of the system, including:
    *   **Infrastructure:** The cloud provider (e.g., {{cloud_provider}}) and the key services used.
    *   **Software:** The application architecture, technologies, and third-party services.
    *   **People:** The roles and responsibilities of the personnel involved in the system's operation, management, and security.
    *   **Processes:** The key processes for change management, incident response, and security monitoring.
    *   **Data:** The types of data processed by the system and the data lifecycle.
4.  **Trust Services Criteria:** A brief statement about which of the five Trust Services Criteria (Security, Availability, Processing Integrity, Confidentiality, Privacy) are included in the scope of the audit.
5.  **System Boundaries:** A clear definition of what is included in the scope of the SOC 2 audit and what is excluded.

Your output should be a well-written and complete System Description that can be used as a key part of the SOC 2 report.
