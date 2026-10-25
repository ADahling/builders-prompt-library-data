---
title: "Write a simple Dockerfile"
slug: write-a-simple-dockerfile
stage: Build
category: "AI Coding Assistants"
grade: B
score: 72
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-a-simple-dockerfile
---
# Write a simple Dockerfile

Generate a Dockerfile for a Node.js 16 application that manages dependencies, exposes port 3000, and configures the container startup.

## Prompt

You are an AI coding assistant. Write a simple Dockerfile for a Node.js application. The Dockerfile should:

- Use the official Node.js 16 image.
- Set the working directory to `/app`.
- Copy the `package.json` and `package-lock.json` files.
- Install the dependencies.
- Copy the rest of the application code.
- Expose port 3000.
- Start the application with `npm start`.

## Tips

Helps enforce good Docker practices from the beginning.
