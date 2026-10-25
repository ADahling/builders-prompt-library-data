---
title: "Implement a CI/CD Pipeline with Security Scanning"
slug: implement-a-ci-cd-pipeline-with-security-scanning
stage: Ship
category: "Deployment & Launch"
grade: B
score: 72
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/implement-a-ci-cd-pipeline-with-security-scanning
---
# Implement a CI/CD Pipeline with Security Scanning

Integrate SAST and SCA scanning into a CI/CD pipeline to automatically detect vulnerabilities and block insecure releases.

Variables: sast_tool_name, sca_tool_name

## Prompt

You are a DevSecOps engineer. Your task is to enhance an existing CI/CD pipeline by adding security scanning stages.

Instructions:
1. Integrate a static application security testing (SAST) tool, like `{{sast_tool_name}}`, to scan the source code for vulnerabilities.
2. Add a software composition analysis (SCA) tool, such as `{{sca_tool_name}}`, to check for known vulnerabilities in third-party dependencies.
3. Configure the pipeline to fail if critical vulnerabilities are found.
4. Generate a security report as part of the pipeline artifacts.

## Tips

This prompt emphasizes the importance of shifting security left and integrating it into the development process.
