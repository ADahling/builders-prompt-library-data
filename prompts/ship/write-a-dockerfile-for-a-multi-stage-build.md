---
title: "Write a Dockerfile for a Multi-stage Build"
slug: write-a-dockerfile-for-a-multi-stage-build
stage: Ship
category: "Deployment & Launch"
grade: A
score: 86
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-a-dockerfile-for-a-multi-stage-build
---
# Write a Dockerfile for a Multi-stage Build

Generate an optimized, production-ready multi-stage Dockerfile that reduces image size and enhances security by isolating build dependencies.

Variables: language

## Prompt

You are a developer tasked with optimizing a Docker image. Write a Dockerfile for a `{{language}}` application that uses a multi-stage build to create a small, secure production image.

Instructions:
1. Use a `builder` stage with the full SDK to build the application.
2. Use a final, smaller stage with only the runtime to run the application.
3. Copy the built artifacts from the `builder` stage to the final stage.
4. Ensure the final image does not contain any build tools or source code.

## Tips

This is a core skill for creating efficient and secure container images.
