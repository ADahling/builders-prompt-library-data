---
title: "Fix a Security Breach from an Insecure Direct Object Reference (IDOR)"
slug: fix-a-security-breach-from-an-insecure-direct-object-reference-idor
stage: Test
category: "Critical Bugs"
grade: B
score: 74
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-a-security-breach-from-an-insecure-direct-object-reference-idor
---
# Fix a Security Breach from an Insecure Direct Object Reference (IDOR)

Remediate IDOR vulnerabilities by implementing session-based ownership checks in backend database queries to prevent unauthorized data access.

## Prompt

You are a web developer. You have discovered a serious security vulnerability in your application. A user can view the data of another user by simply changing the ID in the URL. For example, a user can navigate to `/orders/123` to see their own order, but if they change the URL to `/orders/124`, they can see someone else’s order. This is an Insecure Direct Object Reference (IDOR) vulnerability.

Context:
- The application is a web-based portal for customers to view their own data.
- The backend code retrieves the data from the database based on the ID from the URL, but it does not check if the data belongs to the currently logged-in user.
- The user’s session contains their user ID.

Provide:
1. A clear explanation of the IDOR vulnerability and why it is a critical security risk.
2. The flawed backend code snippet that only uses the object ID to fetch the data.
3. The corrected code that modifies the database query to also include a `WHERE` clause that checks if the object belongs to the currently authenticated user (e.g., `SELECT * FROM orders WHERE id = ? AND user_id = ?`).

## Tips

One of the most common and dangerous web security vulnerabilities.
