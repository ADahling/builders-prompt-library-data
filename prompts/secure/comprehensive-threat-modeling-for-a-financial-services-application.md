---
title: "Comprehensive Threat Modeling for a Financial Services Application"
slug: comprehensive-threat-modeling-for-a-financial-services-application
stage: Secure
category: "Security Review"
grade: A+
score: 96
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/comprehensive-threat-modeling-for-a-financial-services-application
---
# Comprehensive Threat Modeling for a Financial Services Application

Generate a comprehensive PASTA-based threat model for a financial application to identify, prioritize, and mitigate security risks.

Variables: application_name, tech_stack

## Prompt

You are a principal security architect tasked with creating a comprehensive threat model for a new online banking application. The application, named {{application_name}}, is built on a modern technology stack: {{tech_stack}}. It handles sensitive customer financial data, including account balances, transaction histories, and personal identification information.

Your objective is to identify, analyze, and prioritize potential threats to the application and its underlying infrastructure. You must use the PASTA (Process for Attack Simulation and Threat Analysis) methodology. Your threat model should be delivered as a detailed, multi-part report in Markdown format.

The report must include the following sections:

1.  **Stage I: Define Business and Security Objectives:**
    *   Define the business objectives of the application.
    *   Identify the security and compliance requirements (e.g., PCI DSS, GDPR).

2.  **Stage II: Define the Technical Scope:**
    *   Create a detailed architectural diagram of the application.
    *   Identify all components, data flows, and trust boundaries.

3.  **Stage III: Decompose the Application:**
    *   Create data flow diagrams (DFDs) for all key user stories.
    *   Identify all entry points, exit points, and assets.

4.  **Stage IV: Analyze Threats:**
    *   Use a threat intelligence feed (e.g., from a service like Recorded Future or by researching recent financial sector breaches) to identify relevant threats.
    *   Map these threats to the application components.

5.  **Stage V: Analyze Vulnerabilities:**
    *   Correlate the identified threats with potential vulnerabilities in the application and its dependencies.
    *   Use a vulnerability scoring system like CVSS to score the vulnerabilities.

6.  **Stage VI: Model Attacks:**
    *   Create attack trees for the highest-risk threats.
    *   Simulate attack scenarios to understand the potential impact.

7.  **Stage VII: Analyze Risk and Recommend Countermeasures:**
    *   Calculate the risk for each threat.
    *   Provide a prioritized list of detailed, actionable countermeasures and security controls to mitigate the identified risks.

Your final output must be a professional, well-structured report that provides a deep and comprehensive security analysis of the application.
