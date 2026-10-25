---
title: "Network Security Architecture Review for a Hybrid Cloud Environment"
slug: network-security-architecture-review-for-a-hybrid-cloud-environment
stage: Secure
category: "Security Review"
grade: C
score: 65
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/network-security-architecture-review-for-a-hybrid-cloud-environment
---
# Network Security Architecture Review for a Hybrid Cloud Environment

Analyze and harden hybrid cloud infrastructure by auditing segmentation, access controls, and traffic policies to mitigate security risks.

Variables: cloud_provider

## Prompt

You are a network security architect tasked with reviewing the network security architecture of a hybrid cloud environment. The environment consists of an on-premises data center connected to a {{cloud_provider}} VPC via a VPN tunnel. Your goal is to identify and mitigate network security risks.

Your review should include:

1.  **Network Segmentation:** Analyze the VPC and on-premises network segmentation. Ensure that different environments (e.g., production, staging, development) are properly isolated from each other.
2.  **Firewall and Security Group Rules:** Review all firewall rules, security group policies, and network ACLs. Look for overly permissive rules that could allow unauthorized access.
3.  **VPN and Remote Access:** Assess the security of the VPN connection and any other remote access solutions. Verify the authentication and encryption configurations.
4.  **Intrusion Detection and Prevention:** Recommend the placement and configuration of Intrusion Detection Systems (IDS) and Intrusion Prevention Systems (IPS) to monitor for and block malicious network traffic.
5.  **Egress Filtering:** Analyze the outbound traffic rules to prevent data exfiltration. Ensure that only necessary outbound connections are allowed.

For each area, provide a detailed assessment of the current configuration and a list of prioritized recommendations for improvement. Your output should be a comprehensive network security architecture review document in Markdown.
