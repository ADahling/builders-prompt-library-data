---
title: "Using Hashing for Data Integrity"
slug: using-hashing-for-data-integrity
stage: Secure
category: "Security Checklist"
grade: A+
score: 96
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/using-hashing-for-data-integrity
---
# Using Hashing for Data Integrity

Generate and verify SHA-256 checksums to ensure file integrity and detect unauthorized data alterations during transmission.

Variables: file_name

## Prompt

You are learning how to ensure the integrity of data. You have a file that you want to share with a colleague, and you need to make sure the file is not altered in transit. Your task is to use a hashing algorithm to create a checksum for the file.

Context:
- The file is named `{{file_name}}`.
- You are using a command-line tool like `sha256sum` or `md5sum`.

Provide:
1. A brief explanation of what a hashing algorithm is and how it can be used for data integrity.
2. The command to generate a SHA-256 hash of the file.
3. Instructions on how your colleague can verify the integrity of the file using the hash you provide.

## Tips

A simple and practical prompt for understanding the concept of hashing.
