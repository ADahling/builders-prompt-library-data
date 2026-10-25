---
title: "OS Hardening for a Production Web Server"
slug: os-hardening-for-a-production-web-server
stage: Secure
category: "Security Review"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/os-hardening-for-a-production-web-server
---
# OS Hardening for a Production Web Server

Generate a comprehensive, step-by-step Markdown checklist with specific commands to secure and harden a production server’s operating system.

Variables: operating_system

## Prompt

You are a system administrator responsible for deploying a new production web server. The server will be running {{operating_system}} and will host a critical web application. Your task is to harden the operating system to reduce its attack surface and improve its security.

Create a detailed OS hardening checklist in Markdown. The checklist should be a step-by-step guide that can be used to secure the server.

The checklist should cover the following areas:

1.  **Initial Setup:**
    *   Change default passwords.
    *   Configure network settings.
    *   Update the system with the latest security patches.

2.  **User and Group Management:**
    *   Disable the root account.
    *   Create individual user accounts with strong passwords.
    *   Enforce the principle of least privilege.

3.  **Service and Port Management:**
    *   Disable all unnecessary services and ports.
    *   Configure a host-based firewall.

4.  **File System Security:**
    *   Set appropriate file permissions.
    *   Enable file integrity monitoring.

5.  **Logging and Auditing:**
    *   Configure system logging to capture all relevant security events.
    *   Enable auditing.

For each item on the checklist, provide the specific command or configuration change that needs to be made. Your checklist should be a practical and comprehensive guide for hardening a production web server.
