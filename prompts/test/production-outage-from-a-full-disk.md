---
title: "Production Outage from a Full Disk"
slug: production-outage-from-a-full-disk
stage: Test
category: "Critical Bugs"
grade: B
score: 70
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/production-outage-from-a-full-disk
---
# Production Outage from a Full Disk

Resolve a disk-full production outage using emergency access methods, log cleanup commands, and automated log rotation strategies.

## Prompt

You are a junior system administrator. A production server has become unresponsive. Applications are crashing, and you cannot even log in via SSH. You suspect that the server’s root disk is full. Your task is to resolve the issue.

Context:
- The server runs a database that generates large log files.
- The log files have filled up the entire disk.
- You need to free up some space to get the server running again.

Provide:
1. A plan to get access to the server. If SSH is not working, you may need to use a console connection provided by your cloud provider or data center.
2. A sequence of Linux commands (`df -h`, `du -sh *`, `find`) to identify which directory and files are consuming all the disk space.
3. An immediate action plan to free up space (e.g., by deleting or archiving old log files) and a long-term solution to prevent this from happening again, such as setting up log rotation (`logrotate`) and monitoring disk space usage.

## Tips

A very common and basic operational failure that every sysadmin needs to know how to handle.
