---
title: "What is a Canary Token?"
slug: what-is-a-canary-token
stage: Secure
category: "Security Checklist"
grade: B
score: 77
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/what-is-a-canary-token
---
# What is a Canary Token?

Configure and deploy a canary token to proactively detect server breaches through automated alerts triggered by unauthorized file access.

Variables: canary_token_service

## Prompt

You are a security engineer who wants to set up a simple and effective way to get notified if a server is breached. You have decided to use a canary token. Your task is to create a canary token and deploy it on a server.

Context:
- You want to be notified if an attacker gains access to a web server and starts looking around.
- You will use a free canary token service like `{{canary_token_service}}`.

Provide:
1. An explanation of what a canary token is and how it works.
2. A step-by-step guide on how to create a canary token. You should choose a type of token that is likely to be triggered by an attacker, such as a fake AWS API key or a file that looks like a password file.
3. Instructions on how to deploy the canary token on the server and what to do when you receive an alert.

## Tips

A simple, yet clever and effective security technique, presented as a practical task.
