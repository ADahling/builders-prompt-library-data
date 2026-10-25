---
title: "Password Cracking Techniques"
slug: password-cracking-techniques
stage: Secure
category: "Security Checklist"
grade: B
score: 73
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/password-cracking-techniques
---
# Password Cracking Techniques

Demonstrate the vulnerability of weak credentials by using password cracking tools to perform dictionary attacks on test database hashes.

Variables: hash_type, password_cracker

## Prompt

You are a security professional who wants to demonstrate the importance of strong passwords to your development team. You have obtained a list of hashed passwords from a test database, and you want to show how easily weak passwords can be cracked. Your task is to use a password cracking tool to crack some of the passwords.

Context:
- The password hashes are of type `{{hash_type}}` (e.g., MD5, SHA-1, bcrypt).
- You will use a password cracking tool like `{{password_cracker}}` (e.g., John the Ripper, Hashcat).
- You have a wordlist of common passwords.

Provide:
1. An explanation of the difference between a dictionary attack and a brute-force attack.
2. The command to run the password cracker to try to crack the hashes using the wordlist.
3. A summary of the results, including how many passwords were cracked and how long it took. This will be used to make the case for stronger password policies.

## Tips

A hands-on and impactful way to demonstrate the importance of password security.
