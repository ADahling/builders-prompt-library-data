---
title: "Post-Incident Forensic Analysis"
slug: post-incident-forensic-analysis
stage: Secure
category: "Security Checklist"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/post-incident-forensic-analysis
---
# Post-Incident Forensic Analysis

Conduct a comprehensive digital forensic investigation to identify exploit vectors, attacker activity, and data breaches on a compromised CMS.

Variables: operating_system, cms_name

## Prompt

You are a digital forensics investigator who has been called in to analyze a compromised web server. The server was running a popular CMS, and it is suspected that an attacker exploited a known vulnerability to gain access. Your task is to conduct a forensic analysis to determine the extent of the breach and the attacker's actions.

Context:
- The server is running `{{operating_system}}` and the `{{cms_name}}` CMS.
- You have been provided with a disk image of the server's hard drive.

Provide:
1. A list of the initial steps you would take in your forensic analysis (e.g., creating a timeline of events, examining log files, looking for indicators of compromise).
2. A description of the tools you would use for the analysis (e.g., The Sleuth Kit, Volatility Framework).
3. A high-level report of your findings, including the likely attack vector, the actions taken by the attacker, and any data that may have been exfiltrated.

## Tips

A highly specialized and advanced prompt for those interested in digital forensics and incident response.
