---
title: "Docker & Container Best Practices"
slug: docker-container-best-practices
stage: Build
category: "DevOps & IaC"
grade: A
score: 83
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/docker-container-best-practices
---
# Docker & Container Best Practices

Get commented Dockerfile, Compose, and dockerignore files for your app, with multi-stage builds, security settings, and optimization guidance.

## Prompt

Create production-ready Docker configuration for my [describe application]:

1. DOCKERFILE:
   - Multi-stage build (builder → runner)
   - Non-root user for security
   - .dockerignore file
   - Layer optimization (least-changing layers first)
   - Health check
   - Proper signal handling (SIGTERM)

2. DOCKER COMPOSE:
   - Application service
   - Database service (if needed)
   - Environment variable management
   - Volume mounts for persistence
   - Network configuration
   - Resource limits (CPU, memory)

3. SECURITY:
   - No secrets in Dockerfile or image
   - Minimal base image (Alpine or distroless)
   - No unnecessary packages
   - Read-only filesystem where possible
   - Security scanning (Trivy / Snyk)

4. OPTIMIZATION:
   - Image size analysis
   - Build cache strategy
   - Multi-platform builds (amd64 + arm64)

Provide complete Dockerfile, docker-compose.yml, and .dockerignore with comments.

## Tips

Adapted from Firefly.ai and r/devops community prompts. Source: firefly.ai/academy/master-prompt-engineering-top-10
