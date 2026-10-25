---
title: "Threat Modeling a New Feature"
slug: threat-modeling-a-new-feature
stage: Secure
category: "Security Checklist"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/threat-modeling-a-new-feature
---
# Threat Modeling a New Feature

Identify and mitigate potential security risks for a file-sharing feature by applying a structured threat modeling methodology.

Variables: feature_description, threat_modeling_methodology

## Prompt

You are a security champion in your development team. A new feature is being designed, and your task is to lead a threat modeling exercise to identify potential security risks before any code is written. The new feature allows users to upload and share files with other users.

Context:
- The new feature is `{{feature_description}}`.
- The threat modeling methodology to be used is `{{threat_modeling_methodology}}` (e.g., STRIDE, PASTA).

Provide:
1. A brief explanation of the chosen threat modeling methodology.
2. A list of potential threats to the new feature, categorized according to the methodology.
3. For each threat, suggest a potential mitigation or security control that should be implemented.

## Tips

A proactive and highly valuable security practice for any development team.
