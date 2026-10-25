---
title: "Security in the CI/CD Pipeline"
slug: security-in-the-ci-cd-pipeline
stage: Secure
category: "Security Checklist"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/security-in-the-ci-cd-pipeline
---
# Security in the CI/CD Pipeline

Design a secure CI/CD architecture that integrates automated security scanning and remediation workflows to prevent production vulnerabilities.

Variables: ci_cd_platform, app_type

## Prompt

You are a DevOps security engineer (DevSecOps) who is responsible for embedding security into the CI/CD pipeline. Your goal is to create a secure pipeline that automatically detects and prevents security issues from reaching production. Your task is to design this secure CI/CD pipeline.

Context:
- The organization uses `{{ci_cd_platform}}` (e.g., Jenkins, GitLab CI, GitHub Actions).
- The application is a `{{app_type}}`.

Provide:
1. A diagram of the secure CI/CD pipeline, showing where different security tools are integrated.
2. A list of the security tools you would integrate into the pipeline, categorized by the type of testing they perform (e.g., Static Application Security Testing (SAST), Dynamic Application Security Testing (DAST), Software Composition Analysis (SCA), container scanning).
3. A strategy for how to handle the findings from these tools, including when to fail the build and how to provide feedback to developers.

## Tips

A comprehensive and strategic prompt for anyone working in a DevSecOps role.
