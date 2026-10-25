---
title: "Implement a Manual Approval Step for Blue-Green Deployment"
slug: implement-a-manual-approval-step-for-blue-green-deployment
stage: Ship
category: "Deployment & Launch"
grade: C
score: 65
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/implement-a-manual-approval-step-for-blue-green-deployment
---
# Implement a Manual Approval Step for Blue-Green Deployment

Integrate a manual gating mechanism into CI/CD pipelines to validate green environments before executing a production traffic switch.

Variables: ci_cd_tool

## Prompt

You are a release manager. Your task is to add a manual approval gate in your CI/CD pipeline before the traffic switch in a blue-green deployment.

Instructions:
1. In your `{{ci_cd_tool}}` pipeline, add a stage that pauses the deployment after the 'green' environment is verified.
2. The pipeline should wait for a manual approval from a designated person or group.
3. Only after approval should the pipeline proceed with the traffic switch.
4. If rejected, the pipeline should automatically tear down the 'green' environment.

## Tips

Adds a layer of human oversight to automated deployments, which is often required for critical systems.
