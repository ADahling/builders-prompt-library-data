---
title: "Threat Intelligence Feeds"
slug: threat-intelligence-feeds
stage: Secure
category: "Security Checklist"
grade: A
score: 84
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/threat-intelligence-feeds
---
# Threat Intelligence Feeds

Integrate public threat intelligence feeds into a SIEM to automate detection of internal communications with known malicious IP addresses.

Variables: siem_product

## Prompt

You are a security analyst who wants to enrich the data in your SIEM with threat intelligence. You have decided to integrate a threat intelligence feed that provides a list of known malicious IP addresses. Your task is to choose a feed, integrate it into your SIEM, and create a rule that uses the feed.

Context:
- Your SIEM is `{{siem_product}}`.
- You want to detect any communication from your internal network to a known malicious IP address.

Provide:
1. A recommendation for a free and reputable threat intelligence feed that provides a list of malicious IP addresses.
2. A step-by-step guide on how to integrate this feed into your SIEM. This may involve writing a script to download the feed and import it into a lookup table.
3. The pseudo-code or the specific query for a correlation rule that generates an alert when a firewall log shows an outbound connection to an IP address that is in the threat intelligence feed.

## Tips

A practical prompt for security analysts on how to leverage threat intelligence to improve detection capabilities.
