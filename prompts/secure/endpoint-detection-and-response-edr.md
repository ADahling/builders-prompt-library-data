---
title: "Endpoint Detection and Response (EDR)"
slug: endpoint-detection-and-response-edr
stage: Secure
category: "Security Checklist"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/endpoint-detection-and-response-edr
---
# Endpoint Detection and Response (EDR)

Create custom EDR detection rules and investigation workflows to identify process injection techniques using specific MITRE ATT&CK tactics.

Variables: edr_product, tactic_and_technique

## Prompt

You are a security analyst in a SOC that has just deployed a new Endpoint Detection and Response (EDR) solution. You have been tasked with creating a new detection rule to identify a specific attacker technique: process injection. Your goal is to detect when a process, such as `svchost.exe`, is created with a suspicious parent process.

Context:
- The EDR solution is `{{edr_product}}` (e.g., CrowdStrike Falcon, SentinelOne, Microsoft Defender for Endpoint).
- The attacker technique to be detected is `{{tactic_and_technique}}` from the MITRE ATT&CK framework.

Provide:
1. An explanation of the chosen attacker technique and why it is suspicious.
2. The pseudo-code or the specific query for the EDR detection rule.
3. A description of the steps you would take to investigate an alert from this rule to determine if it is a true positive and what to do next.

## Tips

A hands-on prompt for security analysts working with EDR solutions and the MITRE ATT&CK framework.
