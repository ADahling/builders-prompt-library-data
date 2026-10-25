---
title: "Missing or Broken Unsubscribe Link in Marketing Emails"
slug: missing-or-broken-unsubscribe-link-in-marketing-emails
stage: Test
category: "Functional Bugs"
grade: B
score: 75
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/missing-or-broken-unsubscribe-link-in-marketing-emails
---
# Missing or Broken Unsubscribe Link in Marketing Emails

Build a one-click unsubscribe link for marketing emails, with a unique token per subscriber and a backend endpoint that records the opt-out. Check the result against the anti-spam rules where you send.

Variables: project_name, your_domain, unsubscribe_token

## Prompt

You are a developer for {{project_name}}. The marketing team sends out a weekly newsletter. A user has complained that there is no way to unsubscribe from these emails. This is not only a bad user experience but also a violation of anti-spam laws like CAN-SPAM and GDPR, which can lead to legal trouble and your domain being blacklisted.

Your task is to implement a legally compliant one-click unsubscribe mechanism.

**Context:**
- **Problem:** Marketing emails lack a functional unsubscribe link.

**Instructions:**

1.  **Explain the Legal Requirement:** Briefly explain the legal and deliverability-related reasons why every marketing email *must* contain a clear and functional unsubscribe link.
2.  **Generate a Unique Unsubscribe Token:** When sending a marketing email, you need to generate a unique, secure, and user-specific token. This token should be associated with the user's email address in your database.
3.  **Create the Unsubscribe Link:** The unsubscribe link in the email template should point to a dedicated backend endpoint and include this unique token (e.g., `https://{{your_domain}}/unsubscribe?token={{unsubscribe_token}}`).
4.  **Create the Unsubscribe Endpoint:** Create the backend API endpoint (e.g., `GET /unsubscribe`). This endpoint will:
    *   Take the token from the query parameter.
    *   Find the user associated with the token in the database.
    *   Update the user's record to mark them as unsubscribed (e.g., set `is_subscribed = false`).
    *   Display a confirmation page to the user saying they have been successfully unsubscribed.

**Output Format:**

- **Legal Requirement Analysis:** A summary of why this is a critical feature.
- **Unsubscribe Link Generation:** A description of how to create the unique token and link.
- **Unsubscribe Endpoint Code:** The complete code for the backend endpoint that handles the unsubscribe request.

## Tips

A non-negotiable feature for any application that sends non-transactional emails.
