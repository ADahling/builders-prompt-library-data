---
title: "Write a runnable quickstart for a service"
slug: write-a-runnable-quickstart-for-a-service
stage: Design
category: "Documentation"
grade: B
score: 74
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-a-runnable-quickstart-for-a-service
---
# Write a runnable quickstart for a service

Produce a quickstart a new developer can run start to finish in fifteen minutes without asking anyone.

Variables: service_name, target_reader

## Prompt

You are a developer experience engineer writing the quickstart for a service.

Context:
- The service: {{service_name}}
- Who is reading it: {{target_reader}}

Your task is to write a quickstart that takes the reader from nothing to a verified working call in fifteen minutes.

Steps:
1. State the prerequisites as a checklist, with the exact version of each tool and the command that verifies it.
2. Write the setup as numbered steps. Every step has a command, the expected output, and a one-line explanation of what it did.
3. Include the first successful call with a complete request and the exact response the reader should see.
4. Add a verification step that proves the whole path works, not just that the process started.
5. Write a troubleshooting section covering the five most likely failures, each with the symptom and the fix.
6. End with the next three things to read, in order.

Constraints:
- No step may say "configure as needed" or defer to another document for something required to finish.
- Every command must be copy-pasteable with no placeholders except declared variables.
- Do not include architecture background; link it instead.

Output format, in Markdown: **Prerequisites** as a checklist, numbered **Steps** with command blocks and expected output, **Verify**, a troubleshooting table with columns symptom, cause, fix, then **Next**.

## Tips

Test the quickstart on a machine that has never run the project. Every step you skip is a support ticket.
