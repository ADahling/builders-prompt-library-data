---
title: "Identify and Update Outdated Dependencies"
slug: identify-and-update-outdated-dependencies
stage: Test
category: "Cleanup & Warnings"
grade: C
score: 60
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/identify-and-update-outdated-dependencies
---
# Identify and Update Outdated Dependencies

Get a report of outdated dependencies in your package.json, listing the latest available versions and instructions for updating each one.

Variables: project_path

## Prompt

Given the dependencies in the package.json file at {{project_path}}/package.json, identify any dependencies that are outdated. Generate a report listing each outdated dependency along with the latest version available and instructions for updating.

## Tips

Keeping dependencies up to date is crucial for security and performance.
