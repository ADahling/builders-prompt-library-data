---
title: "Implement Strong Password Policies"
slug: implement-strong-password-policies
stage: Secure
category: "Security Checklist"
grade: A+
score: 93
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/implement-strong-password-policies
---
# Implement Strong Password Policies

Establish secure password criteria, user-friendly validation messages, and safe storage methods for a specific authentication system.

Variables: app_type, authentication_library

## Prompt

You are building a new user authentication system and need to enforce strong password policies. Your goal is to guide users to create secure passwords without making the process overly complex. The current system only requires a minimum of 6 characters.

Context:
- The application is a {{app_type}}.
- You are using {{authentication_library}} for user management.

Provide:
1. A list of recommended password policy rules (e.g., minimum length, character types).
2. A user-friendly error message to display when a password does not meet the criteria.
3. A suggestion for how to securely store user passwords in the database.

## Tips

A fundamental prompt for anyone building a system with user accounts.
