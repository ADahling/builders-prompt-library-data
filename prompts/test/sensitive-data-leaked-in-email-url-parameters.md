---
title: "Sensitive Data Leaked in Email URL Parameters"
slug: sensitive-data-leaked-in-email-url-parameters
stage: Test
category: "Functional Bugs"
grade: A+
score: 94
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/sensitive-data-leaked-in-email-url-parameters
---
# Sensitive Data Leaked in Email URL Parameters

Secure user privacy by refactoring password reset flows to eliminate PII from URL parameters through token-based database lookups.

Variables: project_name, your_domain, reset_token

## Prompt

You are a security engineer for {{project_name}}. A password reset email is being sent to users with a link like this: `https://{{your_domain}}/reset-password?email=user@example.com&reset_token=...`. The user's email address is being passed directly in the URL's query parameters.

This is a security vulnerability. URLs can be logged in browser history, web server logs, and by intermediate proxies, potentially exposing the user's email address in connection with a password reset action.

Your task is to fix this by removing the identifying information from the URL.

**Context:**
- **Problem:** Leaking Personally Identifiable Information (PII) in URL parameters.

**Instructions:**

1.  **Explain the Security Risk:** Describe the risks of putting sensitive or personally identifiable information in URL query parameters. Explain where these URLs can be logged and who might be able to see them.
2.  **Refactor the Token Strategy:** The `reset_token` should be the *only* piece of information needed to identify the user and authorize the password reset. When you generate the reset token, you must store it in your database and associate it with the user's ID and an expiration timestamp.
3.  **Refactor the Endpoint and Link:**
    *   The link in the email should now be clean: `https://{{your_domain}}/reset-password?token={{reset_token}}`.
    *   The backend endpoint that handles this link will now look up the user *by the token*, not by an email address passed in the URL. It should also verify that the token has not expired.

**Output Format:**

- **Security Risk Analysis:** A clear explanation of the PII leakage vulnerability.
- **Refactored Token Strategy:** A description of how the token should be stored and associated with the user in the database.
- **Corrected Backend Endpoint Logic:** The code for the backend endpoint that securely looks up the user by the token alone.

## Tips

A subtle but important security hardening practice for a common email-related feature.
