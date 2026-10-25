---
title: "Directory Traversal Attack Prevention"
slug: directory-traversal-attack-prevention
stage: Secure
category: "Security Checklist"
grade: A+
score: 94
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/directory-traversal-attack-prevention
---
# Directory Traversal Attack Prevention

Implement robust file path validation and sanitization to prevent directory traversal vulnerabilities in a specific programming language.

Variables: programming_language, base_directory, filename_parameter

## Prompt

You are a web developer who is building a feature that allows users to view files from a specific directory on the server. You are concerned about directory traversal attacks, where an attacker could access files outside of the intended directory. Your task is to write secure code that prevents this attack.

Context:
- The application is written in `{{programming_language}}`.
- The files are supposed to be served from the `{{base_directory}}` directory.
- The user provides a filename as a request parameter: `{{filename_parameter}}`.

Provide:
1. An explanation of what a directory traversal attack is and an example of a malicious filename that an attacker might use.
2. A code example of vulnerable code that is susceptible to directory traversal.
3. A code example of secure code that properly validates the user-supplied filename and ensures that it is within the base directory.

## Tips

A practical prompt for preventing a classic web security vulnerability.
