---
title: "Generate a Kubernetes deployment configuration"
slug: generate-a-kubernetes-deployment-configuration
stage: Build
category: "AI Coding Assistants"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-a-kubernetes-deployment-configuration
---
# Generate a Kubernetes deployment configuration

Generate a Kubernetes deployment configuration for a containerized app: deployment, service, replicas, resource limits, and health probes.

Variables: image_name, port, replica_count

## Prompt

You have a containerized application. Your task is to use an AI coding assistant to generate a Kubernetes deployment configuration for it.

The application image is `{{image_name}}` and it listens on port `{{port}}`.

Generate a Kubernetes deployment YAML file that includes:
1. A deployment with `{{replica_count}}` replicas.
2. A service of type `LoadBalancer` to expose the application.

## Tips

Automates the creation of Kubernetes configuration files.
