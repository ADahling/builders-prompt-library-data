---
title: "Security Requirements for a New E-commerce Website"
slug: security-requirements-for-a-new-e-commerce-website
stage: Secure
category: "Security Review"
grade: A+
score: 95
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/security-requirements-for-a-new-e-commerce-website
---
# Security Requirements for a New E-commerce Website

Generate a comprehensive, SMART-compliant security requirements document for an e-commerce platform covering PCI DSS, GDPR, and OWASP standards.

Variables: website_name

## Prompt

You are a product manager for a new e-commerce website, {{website_name}}. You are in the process of writing the product requirements document (PRD). You need to include a section on security requirements to ensure the website is built with security in mind from the beginning.

Create a detailed list of security requirements for the e-commerce website. The requirements should be in Markdown format and should be specific, measurable, achievable, relevant, and time-bound (SMART).

The security requirements should cover the following areas:

1.  **Authentication and Account Management:**
    *   Users must be able to create an account with a unique email address and a strong password.
    *   The website must support two-factor authentication (2FA).
    *   The website must have a secure password reset process.

2.  **Payment Processing:**
    *   The website must be PCI DSS compliant.
    *   All payment information must be encrypted in transit and at rest.
    *   The website must not store credit card numbers.

3.  **Data Privacy:**
    *   The website must have a clear privacy policy.
    *   The website must be GDPR compliant.
    *   Users must be able to view, edit, and delete their personal data.

4.  **Application Security:**
    *   The website must be protected against the OWASP Top 10 vulnerabilities.
    *   The website must have a Web Application Firewall (WAF).
    *   The website must undergo regular penetration testing.

5.  **Infrastructure Security:**
    *   The website must be hosted on a secure cloud provider.
    *   The infrastructure must be protected by a firewall and other security measures.

Your list of security requirements should be comprehensive and provide a solid foundation for building a secure e-commerce website.
