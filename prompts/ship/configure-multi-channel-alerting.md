---
title: "Configure Multi-Channel Alerting"
slug: configure-multi-channel-alerting
stage: Ship
category: "Deployment & Launch"
grade: C
score: 61
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/configure-multi-channel-alerting
---
# Configure Multi-Channel Alerting

Automate severity-based notifications across chat, email, and on-call tools to ensure critical incidents receive immediate attention.

Variables: alerting_tool, chat_tool, on_call_tool

## Prompt

You are an IT administrator. Configure your alerting system (`{{alerting_tool}}`) to send notifications to multiple channels based on the severity of the alert.

Instructions:
1. Low-severity alerts should be sent to a chat channel (`{{chat_tool}}`).
2. High-severity alerts should be sent to the chat channel and also as an email.
3. Critical alerts should page the on-call engineer via a tool like `{{on_call_tool}}`.
4. This ensures that alerts get the right level of attention.

## Tips

A basic but important aspect of a well-configured alerting system.
