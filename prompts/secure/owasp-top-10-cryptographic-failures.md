---
title: "OWASP Top 10: Cryptographic Failures"
slug: owasp-top-10-cryptographic-failures
stage: Secure
category: "Security Checklist"
grade: A+
score: 91
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/owasp-top-10-cryptographic-failures
---
# OWASP Top 10: Cryptographic Failures

Identify cryptographic weaknesses in legacy code and implement secure migration strategies using modern encryption standards.

Variables: data_to_be_encrypted, weak_algorithm

## Prompt

You are reviewing a piece of code that is responsible for encrypting sensitive data before storing it in a database. You have noticed that the code is using an outdated and weak encryption algorithm. Your task is to identify the weakness and recommend a more secure alternative.

Context:
- The sensitive data is `{{data_to_be_encrypted}}`.
- The current code uses the `{{weak_algorithm}}` algorithm (e.g., DES, MD5 for hashing passwords).

Provide:
1. An explanation of why the current encryption algorithm is considered weak and should not be used.
2. A recommendation for a modern, strong encryption algorithm to replace the weak one (e.g., AES-256 for encryption, bcrypt or Argon2 for password hashing).
3. A high-level plan for how to migrate from the old algorithm to the new one, including how to handle existing data that was encrypted with the weak algorithm.

## Tips

A crucial prompt for ensuring the confidentiality of sensitive data.
