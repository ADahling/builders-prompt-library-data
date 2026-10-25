---
title: "Orchestrate a Rolling Update in Kubernetes"
slug: orchestrate-a-rolling-update-in-kubernetes
stage: Ship
category: "Deployment & Launch"
grade: B
score: 76
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/orchestrate-a-rolling-update-in-kubernetes
---
# Orchestrate a Rolling Update in Kubernetes

Execute a zero-downtime rolling update in Kubernetes by deploying new image versions, monitoring rollout status, and managing rollbacks.

Variables: new_image_version

## Prompt

You are a Kubernetes operator. Perform a rolling update for a deployment to a new container image version, `{{new_image_version}}`, with zero downtime.

Instructions:
1. Update the image for the deployment using `kubectl set image`.
2. Monitor the status of the rolling update using `kubectl rollout status`.
3. Verify that the new version is running correctly.
4. Demonstrate how to roll back to the previous version if something goes wrong.

## Tips

A core competency for managing applications on Kubernetes.
