---
title: "Optimize a Docker Image for Production"
slug: optimize-a-docker-image-for-production
stage: Ship
category: "Deployment & Launch"
grade: C
score: 62
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/optimize-a-docker-image-for-production
---
# Optimize a Docker Image for Production

Minimize Python Docker image size and enhance security by implementing multi-stage builds, slim base images, and non-root user execution.

## Prompt

You are a performance engineer. Your task is to optimize a Docker image for a Python application to reduce its size and improve security.

Instructions:
1. Use a multi-stage build to separate the build environment from the runtime environment.
2. Start from a minimal base image like `python:3.9-slim`.
3. Ensure that only the necessary application code and dependencies are copied into the final image.
4. Run the container as a non-root user to enhance security.

## Tips

This prompt teaches important best practices for creating production-ready Docker images.
