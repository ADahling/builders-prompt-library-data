---
title: "Investigate Production Outage Caused by Configuration Change"
slug: investigate-production-outage-caused-by-configuration-change
stage: Test
category: "Critical Bugs"
grade: C
score: 65
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/investigate-production-outage-caused-by-configuration-change
---
# Investigate Production Outage Caused by Configuration Change

Identify, revert, and prevent faulty Ansible configuration changes causing production outages through rollback procedures and safer deployments.

## Prompt

You are a DevOps engineer. A recent configuration change pushed to production has caused a major outage. Your task is to quickly identify the problematic change and roll it back.

Context:
- The configuration is managed using Ansible.
- The change was intended to update the firewall rules on a cluster of web servers.
- The outage began immediately after the new configuration was applied.

Provide:
1. The command to view the history of Ansible playbook runs and identify the exact change that was made.
2. A step-by-step guide to revert the change and restore the previous working configuration.
3. A proposal for a safer configuration deployment process, including testing and canary releases.

## Tips

Focuses on incident response in a DevOps context.
