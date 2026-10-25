---
title: "Scan Docker Images for Vulnerabilities"
slug: scan-docker-images-for-vulnerabilities
stage: Ship
category: "Deployment & Launch"
grade: B
score: 72
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/scan-docker-images-for-vulnerabilities
---
# Scan Docker Images for Vulnerabilities

Automate container security audits by integrating automated image scanning into CI/CD pipelines to block vulnerable deployments.

Variables: vulnerability_scanner

## Prompt

You are a security engineer. Integrate a tool like `{{vulnerability_scanner}}` into your CI/CD pipeline to scan Docker images for known vulnerabilities before they are deployed.

Instructions:
1. Add a stage in your pipeline that runs after the Docker image is built.
2. Run the scanner against the newly built image.
3. Fail the pipeline if any high-severity vulnerabilities are found.
4. Generate a report of the findings.

## Tips

A critical step in securing your containerized applications.
