---
title: "Create a Performance-Optimized Docker Image for a Node.js App"
slug: create-a-performance-optimized-docker-image-for-a-node-js-app
stage: Test
category: "Performance & Code"
grade: A
score: 87
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-performance-optimized-docker-image-for-a-node-js-app
---
# Create a Performance-Optimized Docker Image for a Node.js App

Get a multi-stage Node.js Dockerfile and production guidance on base images, dependencies, non-root users, and image size optimization.

Variables: AppName

## Prompt

I need to create a Docker image for our Node.js application, `{{AppName}}`, that is both small and secure. The goal is to optimize the image for production deployment, focusing on performance and a minimal attack surface.

Your task is to provide a `Dockerfile` and a set of best practices for building a production-ready Docker image for a Node.js application.

Your response should include:
1.  **Multi-Stage Dockerfile:** A complete, well-commented `Dockerfile` that uses multi-stage builds to create a small production image. The `Dockerfile` should handle dependency installation, code copying, and running the application.
2.  **Base Image Selection:** A discussion of how to choose the right base image for a Node.js application, with a recommendation for a small and secure option like `node:alpine`.
3.  **Dependency Management:** Best practices for managing `npm` dependencies in a Dockerfile, including using `npm ci` for deterministic builds and avoiding the installation of unnecessary `devDependencies`.
4.  **Security Best Practices:** A set of security recommendations for the Docker image, such as running the application as a non-root user and using a `.dockerignore` file to avoid copying sensitive files into the image.
5.  **Optimization Techniques:** Additional optimization techniques, such as using a smaller `npm` client like `pnpm` or `yarn` and cleaning up the `npm` cache.
