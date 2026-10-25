---
title: "Debug a memory leak in a Node.js application with Windsurf"
slug: debug-a-memory-leak-in-a-node-js-application-with-windsurf
stage: Build
category: "AI Coding Assistants"
grade: C
score: 63
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/debug-a-memory-leak-in-a-node-js-application-with-windsurf
---
# Debug a memory leak in a Node.js application with Windsurf

Identify and resolve Node.js memory leaks by capturing heap snapshots and analyzing object growth within a specific module using Windsurf.

Variables: module_name

## Prompt

You are debugging a Node.js application with Windsurf. The application has a memory leak, and you suspect it is related to a specific module, `{{module_name}}`.

Describe the prompts and workflow you would use in Windsurf to:
1. Take heap snapshots of the application at different times.
2. Compare the snapshots to identify growing objects.
3. Pinpoint the source of the leak in the `{{module_name}}` module.

## Tips

A scenario-based prompt for using a specific AI tool for debugging memory leaks.
