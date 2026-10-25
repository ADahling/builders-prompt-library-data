---
title: "Proactively Manage Deprecations with Automated Tooling"
slug: proactively-manage-deprecations-with-automated-tooling
stage: Test
category: "Cleanup & Warnings"
grade: A
score: 83
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/proactively-manage-deprecations-with-automated-tooling
---
# Proactively Manage Deprecations with Automated Tooling

Design a workflow to track dependency deprecations, create issues automatically, and apply codemods, with scripts or CI configuration examples.

Variables: language, issue_tracker

## Prompt

I want to set up a system to proactively manage deprecations in my {{language}} project. Instead of waiting for warnings to appear, I want to be notified of upcoming deprecations and have a clear plan to address them. 

Your task is to design a workflow for this. Please cover the following:

1.  **Deprecation Tracking:** How can I track deprecations in my project's dependencies? Are there tools or services that can scan my `package.json` or `requirements.txt` and report on upcoming or existing deprecations?
2.  **Automated Issue Creation:** I want to automatically create issues in my issue tracker ({{issue_tracker}}) whenever a new deprecation is detected. Provide a script or a CI/CD pipeline configuration to achieve this. The issue should contain details about the deprecated API, the suggested replacement, and a link to the relevant documentation.
3.  **Codemods for Automatic Updates:** For common deprecations, I want to use codemods to automatically update the codebase. Explain what codemods are and how to use them in a {{language}} project. Provide an example of a simple codemod to fix a hypothetical deprecation.

Output should be a comprehensive guide with practical examples and configuration snippets.

## Tips

This prompt focuses on a proactive, automated approach to technical debt management.
