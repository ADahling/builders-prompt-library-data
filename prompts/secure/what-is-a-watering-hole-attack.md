---
title: "What is a Watering Hole Attack?"
slug: what-is-a-watering-hole-attack
stage: Secure
category: "Security Checklist"
grade: A+
score: 90
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/what-is-a-watering-hole-attack
---
# What is a Watering Hole Attack?

Analyze a specific watering hole attack to reconstruct the exploit chain and generate a professional threat intelligence report.

Variables: website_name, target_group, vulnerable_software

## Prompt

You are a threat intelligence analyst who is investigating a watering hole attack. The attacker has compromised a website that is popular with a specific group of people and has used it to deliver malware to them. Your task is to analyze the attack and to create a report.

Context:
- The compromised website is `{{website_name}}`.
- The target group is `{{target_group}}`.
- The attacker used a zero-day exploit for `{{vulnerable_software}}`.

Provide:
1. An explanation of what a watering hole attack is and how it works.
2. A step-by-step reconstruction of the attack chain, from the initial compromise of the website to the delivery of the malware to the victims.
3. A list of recommendations for how to defend against watering hole attacks, both for website owners and for end-users.

## Tips

A practical prompt that deals with a sophisticated and targeted type of attack.
