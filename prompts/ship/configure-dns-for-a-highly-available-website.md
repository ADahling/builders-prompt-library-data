---
title: "Configure DNS for a Highly Available Website"
slug: configure-dns-for-a-highly-available-website
stage: Ship
category: "Deployment & Launch"
grade: A
score: 83
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/configure-dns-for-a-highly-available-website
---
# Configure DNS for a Highly Available Website

Implement DNS round-robin by mapping multiple server IPs to a single domain to improve traffic distribution and website availability.

Variables: ip_address_1, ip_address_2, domain_name

## Prompt

You are a network engineer. Configure DNS for a website to be highly available by using multiple IP addresses for the same domain.

Instructions:
1. Your website is hosted on two servers with IP addresses `{{ip_address_1}}` and `{{ip_address_2}}`.
2. Create two `A` records for your domain, `{{domain_name}}`, one for each IP address.
3. Explain how DNS round-robin works to distribute traffic between the two servers.
4. Discuss the limitations of this approach for failover.

## Tips

A simple way to achieve a basic level of high availability.
