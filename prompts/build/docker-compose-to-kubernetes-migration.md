---
title: "Docker Compose to Kubernetes Migration"
slug: docker-compose-to-kubernetes-migration
stage: Build
category: "DevOps & IaC"
grade: B
score: 73
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/docker-compose-to-kubernetes-migration
---
# Docker Compose to Kubernetes Migration

Turn a web app and Postgres Compose file into commented Kubernetes YAML with a Deployment, Service, PersistentVolumeClaim, and resource limits.

## Prompt

Here's my Docker Compose file for a web app and Postgres: [paste file]. Convert it to Kubernetes manifests, including a Deployment, Service, and PersistentVolumeClaim. Use best practices like resource limits, labels, and namespaces. Output as separate YAML files with comments.

## Tips

Docker Compose → K8s is the most common migration path. Source: medium.com/@onix_react/ultimate-prompts-for-every-developer
