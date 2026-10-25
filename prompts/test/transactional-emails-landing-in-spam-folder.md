---
title: "Transactional Emails Landing in Spam Folder"
slug: transactional-emails-landing-in-spam-folder
stage: Test
category: "Functional Bugs"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/transactional-emails-landing-in-spam-folder
---
# Transactional Emails Landing in Spam Folder

Implement SPF, DKIM, and DMARC protocols to resolve email deliverability issues and prevent transactional messages from being flagged as spam.

Variables: project_name, your_domain, email_service_provider

## Prompt

You are a backend developer for {{project_name}}, an e-commerce platform. Users are reporting that they are not receiving critical transactional emails, such as order confirmations and password resets. An investigation reveals that these emails are being sent but are frequently landing in the users' spam folders.

This is likely due to a lack of proper email authentication protocols (SPF, DKIM, DMARC) and a poor sender reputation.

**Context:**
- **Problem:** Emails sent from your application server are being flagged as spam.

**Instructions:**

1.  **Explain Email Authentication:** Describe the purpose of SPF (Sender Policy Framework), DKIM (DomainKeys Identified Mail), and DMARC (Domain-based Message Authentication, Reporting, and Conformance). Explain how these DNS records prove to receiving email servers that your server is authorized to send emails on behalf of your domain (e.g., `{{your_domain}}`).
2.  **Provide DNS Record Examples:** Give examples of the DNS `TXT` records that need to be added to your domain's DNS settings to implement SPF and DMARC.
3.  **Explain DKIM Setup:** Describe the process of generating a public/private key pair for DKIM. The private key is used by your email sending service/library to sign outgoing emails, and the public key is published in a DNS `TXT` record.
4.  **Recommend a Transactional Email Service:** Strongly recommend switching from sending emails directly from your application server to using a dedicated transactional email service (e.g., {{email_service_provider}}). Explain that these services are experts in deliverability and handle all of these authentication and reputation issues for you.

**Output Format:**

- **Email Authentication Analysis:** A clear explanation of SPF, DKIM, and DMARC.
- **DNS Record Examples:** The sample `TXT` records for SPF and DMARC.
- **DKIM Setup Overview:** A summary of the DKIM key generation and signing process.
- **Service Recommendation:** A strong recommendation to use a professional email service.

## Tips

A critical deliverability issue that almost every application faces. This prompt teaches the fundamentals of not landing in spam.
