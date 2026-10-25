---
title: "EC2 Health Monitoring Bash Script"
slug: ec2-health-monitoring-bash-script
stage: Build
category: "DevOps & IaC"
grade: A
score: 85
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/ec2-health-monitoring-bash-script
---
# EC2 Health Monitoring Bash Script

Write an AWS CLI Bash script to check EC2 in us-west-2 every five minutes, handle CLI errors, and send Slack alerts for stopped instances.

## Prompt

Write a bash script using AWS CLI to check the status of all EC2 instances in us-west-2. Include error handling for AWS CLI failures, a loop to check every 5 minutes, and a Slack notification (via webhook) if any instance is stopped. Add comments explaining each section. Return the script in a code block.

## Tips

A practical script you can actually run in production. Source: medium.com/@onix_react/ultimate-prompts-for-every-developer
