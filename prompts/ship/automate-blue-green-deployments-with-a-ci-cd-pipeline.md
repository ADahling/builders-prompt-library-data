---
title: "Automate Blue-Green Deployments with a CI/CD Pipeline"
slug: automate-blue-green-deployments-with-a-ci-cd-pipeline
stage: Ship
category: "Deployment & Launch"
grade: B
score: 77
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/automate-blue-green-deployments-with-a-ci-cd-pipeline
---
# Automate Blue-Green Deployments with a CI/CD Pipeline

Automate zero-downtime blue-green deployments including environment provisioning, health validation, and traffic switching via CI/CD pipelines.

Variables: ci_cd_tool, scripting_language

## Prompt

You are a DevOps architect. Design and implement a fully automated blue-green deployment pipeline using `{{ci_cd_tool}}` and `{{scripting_language}}`.

Instructions:
1. The pipeline should provision a new 'green' environment from scratch.
2. It should deploy the new application version to the green environment.
3. It must run a comprehensive suite of automated end-to-end tests.
4. If tests pass, it should automatically switch traffic and then de-provision the old 'blue' environment.

## Tips

This prompt requires a deep understanding of both CI/CD and deployment strategies.
