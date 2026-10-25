---
title: "Troubleshoot High CPU Usage in a Production Server"
slug: troubleshoot-high-cpu-usage-in-a-production-server
stage: Test
category: "Critical Bugs"
grade: C
score: 67
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/troubleshoot-high-cpu-usage-in-a-production-server
---
# Troubleshoot High CPU Usage in a Production Server

Identify and resolve Linux server CPU spikes using command-line diagnostics, process investigation techniques, and root cause analysis.

## Prompt

You are a system administrator. A production Linux server is experiencing sustained high CPU usage (near 100%), making the applications running on it slow and unresponsive. Your task is to identify the process causing the high CPU usage and resolve the issue.

Context:
- The server hosts a variety of services, including a web server, a database, and some background jobs.
- You have shell access to the server.
- The issue started recently, but the exact cause is unknown.

Provide:
1. A sequence of Linux commands (like `top`, `htop`, `ps`) to identify the specific process or thread that is consuming the most CPU.
2. A strategy to investigate the identified process further. For example, if it's a Java process, how would you use tools like `jstack` to see what the threads are doing?
3. A list of common causes for high CPU usage, such as infinite loops in code, inefficient algorithms, or poorly configured services.

## Tips

A fundamental troubleshooting skill for any system administrator or DevOps engineer.
