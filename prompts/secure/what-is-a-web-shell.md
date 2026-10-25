---
title: "What is a Web Shell?"
slug: what-is-a-web-shell
stage: Secure
category: "Security Checklist"
grade: B
score: 79
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/what-is-a-web-shell
---
# What is a Web Shell?

Analyze a suspicious file to determine its functionalities and identify indicators of compromise for detecting web shells on a server.

Variables: web_server_software, programming_language, file_name, file_type

## Prompt

You are a security analyst who is investigating a compromised web server. You have found a suspicious file on the server that you believe is a web shell. Your task is to analyze the web shell and to understand its capabilities.

Context:
- The web server is running `{{web_server_software}}` and `{{programming_language}}`.
- The suspicious file is named `{{file_name}}` and it is a `{{file_type}}` file.

Provide:
1. An explanation of what a web shell is and how an attacker can use it.
2. An analysis of the web shell's code, explaining its key functionalities (e.g., file upload, command execution, database connection).
3. A list of indicators of compromise (IOCs) that you can use to search for other web shells on your network.

## Tips

A hands-on prompt for security analysts on how to analyze a common post-exploitation tool.
