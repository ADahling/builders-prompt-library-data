---
title: "Docker Multi-Stage Build Optimizer"
slug: docker-multi-stage-build-optimizer
stage: Build
category: "DevOps & IaC"
grade: A+
score: 94
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/docker-multi-stage-build-optimizer
---
# Docker Multi-Stage Build Optimizer

Refactor Dockerfiles into secure, multi-stage builds to minimize image size and maximize layer caching performance.

Variables: application_name, current_dockerfile

## Prompt

You are a container optimization specialist. Optimize the Docker build for {{application_name}}.

Current Dockerfile:
{{current_dockerfile}}

Optimize for:
1. **Multi-Stage Build**: Separate build and runtime stages
2. **Image Size**: Minimize final image size (target: <100MB for Node.js apps)
3. **Build Cache**: Maximize layer caching for faster rebuilds
4. **Security**: Non-root user, minimal base image, no secrets in layers
5. **Dependencies**: Only production dependencies in final image
6. **Health Check**: Built-in health check instruction
7. **.dockerignore**: Comprehensive ignore file
8. **Build Arguments**: Parameterize for different environments

Provide:
- Optimized Dockerfile with comments explaining each decision
- docker-compose.yml for local development
- Size comparison: before vs after
- Build time comparison: cold build vs cached rebuild

## Tips

A well-optimized Docker image deploys faster, uses less storage, and has a smaller attack surface.
