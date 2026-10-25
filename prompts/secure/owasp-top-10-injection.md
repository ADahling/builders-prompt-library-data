---
title: "OWASP Top 10: Injection"
slug: owasp-top-10-injection
stage: Secure
category: "Security Checklist"
grade: A+
score: 94
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/owasp-top-10-injection
---
# OWASP Top 10: Injection

Generate secure, parameterized database queries to prevent SQL injection vulnerabilities while contrasting them with insecure coding practices.

Variables: database_type, programming_language

## Prompt

You are a developer who needs to write a database query that includes user-supplied input. You are aware of SQL injection and want to make sure your code is not vulnerable. Your task is to write a secure database query using parameterized statements (prepared statements).

Context:
- The database is `{{database_type}}`.
- The programming language is `{{programming_language}}`.
- You need to fetch a user's profile based on their email address, which is provided by the user.

Provide:
1. A code example of a vulnerable SQL query that uses string concatenation.
2. A code example of a secure SQL query that uses parameterized statements to prevent SQL injection.
3. An explanation of why the parameterized query is secure and the vulnerable query is not.

## Tips

A practical, hands-on prompt for learning the most important defense against SQL injection.
