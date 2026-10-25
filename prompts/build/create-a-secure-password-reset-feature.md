---
title: "Create a Secure Password Reset Feature"
slug: create-a-secure-password-reset-feature
stage: Build
category: "Backend & Data Integrity"
grade: A+
score: 92
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-secure-password-reset-feature
---
# Create a Secure Password Reset Feature

Design an app password reset flow with token generation and storage, an email template, attack mitigations, and a high-level code example.

Variables: application_name, programming_language

## Prompt

I need to implement a secure password reset feature for our {{application_name}} application. The feature must be secure against common attacks like session hijacking and token theft.

Your task is to design a secure password reset feature. The design should include:

1.  **Workflow:** A step-by-step workflow for the password reset process. This should include generating a unique and time-limited reset token, sending the token to the user's email address, and allowing the user to reset their password after verifying the token.
2.  **Token Generation and Storage:** A secure way to generate and store the password reset tokens. The tokens should be random, unpredictable, and should be stored in a way that they cannot be easily stolen.
3.  **Email Template:** A secure and user-friendly email template for the password reset email. The email should clearly explain what to do and should not reveal any sensitive information.
4.  **Security Considerations:** A discussion of the security risks associated with password reset features and how to mitigate them. This should include protection against brute-force attacks, token leakage, and phishing attacks.
5.  **Code Example:** A high-level code example in {{programming_language}} that illustrates the key components of the password reset feature.

## Tips

This prompt is a fundamental security feature for any application that has user accounts.
