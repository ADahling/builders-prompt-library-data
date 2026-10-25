---
title: "What is a DMZ?"
slug: what-is-a-dmz
stage: Secure
category: "Security Checklist"
grade: B
score: 70
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/what-is-a-dmz
---
# What is a DMZ?

Design a three-interface firewall architecture with a DMZ, network diagram, and specific traffic rules to secure public-facing web servers.

## Prompt

You are a network architect designing the network for a new office. You need to host a public-facing web server, and you want to do it securely. You have decided to use a DMZ (Demilitarized Zone) to isolate the web server from the internal network. Your task is to design the DMZ architecture.

Context:
- You have one firewall with at least three interfaces.
- The web server needs to be accessible from the internet on port 443.
- The internal network should be able to access the internet, but the internet should not be able to access the internal network directly.

Provide:
1. An explanation of what a DMZ is and why it is used.
2. A network diagram showing the firewall, the internet, the DMZ, and the internal network. The diagram should show the IP addressing scheme for each zone.
3. The firewall rules (in a generic format) that you would configure to implement this DMZ. The rules should specify the source, destination, and port for each allowed traffic flow.

## Tips

A classic network security concept, presented as a practical design task.
