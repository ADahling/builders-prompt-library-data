---
title: "Set up an On-Call Rotation and Escalation Policy"
slug: set-up-an-on-call-rotation-and-escalation-policy
stage: Ship
category: "Deployment & Launch"
grade: C
score: 67
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/set-up-an-on-call-rotation-and-escalation-policy
---
# Set up an On-Call Rotation and Escalation Policy

Establish structured on-call schedules and multi-level escalation policies to ensure rapid incident response and clear team accountability.

Variables: on_call_tool

## Prompt

You are a manager of an engineering team. Your task is to set up an on-call rotation and an escalation policy for your team using a tool like `{{on_call_tool}}`.

Instructions:
1. Create a schedule for the on-call rotation.
2. Define different levels of alerts (e.g., P1, P2, P3).
3. For each alert level, define who should be notified and how (e.g., P1 alerts page the on-call engineer immediately).
4. Define an escalation policy if the on-call engineer does not acknowledge an alert within a certain time.

## Tips

A crucial part of running a reliable service is having a well-defined incident response process.
