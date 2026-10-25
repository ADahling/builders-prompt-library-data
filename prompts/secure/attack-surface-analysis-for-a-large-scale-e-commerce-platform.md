---
title: "Attack Surface Analysis for a Large-Scale E-commerce Platform"
slug: attack-surface-analysis-for-a-large-scale-e-commerce-platform
stage: Secure
category: "Security Review"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/attack-surface-analysis-for-a-large-scale-e-commerce-platform
---
# Attack Surface Analysis for a Large-Scale E-commerce Platform

Generate a comprehensive security audit report identifying entry points, data flows, and prioritized remediations for an e-commerce platform.

Variables: platform_name, tech_stack

## Prompt

You are a security consultant hired to perform an attack surface analysis for a large-scale e-commerce platform, {{platform_name}}. The platform has a complex architecture, including a customer-facing website, a mobile app, a vendor portal, and numerous backend microservices. The technology stack is {{tech_stack}}.

Your goal is to identify all potential entry points for attackers and assess the overall attack surface of the platform. Your analysis should be structured and methodical.

Please provide a detailed report in Markdown that covers the following:

1.  **Asset and Entry Point Identification:**
    *   Identify all external assets, including domain names, IP addresses, and open ports.
    *   Map out all user-facing interfaces (web, mobile, API) and administrative interfaces.
    *   Identify all third-party integrations and their potential security implications.

2.  **Technology and Framework Profiling:**
    *   Identify all technologies, frameworks, and libraries used in the platform.
    *   Research known vulnerabilities associated with these technologies.

3.  **User and Role Analysis:**
    *   Identify all user roles (e.g., customer, vendor, administrator) and their associated privileges.
    *   Analyze the potential for privilege escalation attacks.

4.  **Data Flow Analysis:**
    *   Trace the flow of sensitive data (e.g., payment information, personal data) through the platform.
    *   Identify points where data could be intercepted or exfiltrated.

5.  **Attack Surface Visualization:**
    *   Create a visual representation of the attack surface, such as a mind map or a diagram.

6.  **Prioritized Recommendations:**
    *   Based on your analysis, provide a prioritized list of recommendations to reduce the attack surface. These could include disabling unused services, restricting access to interfaces, and implementing additional security controls.

Your report should be comprehensive and provide the company with a clear understanding of its security posture and a roadmap for improvement.
