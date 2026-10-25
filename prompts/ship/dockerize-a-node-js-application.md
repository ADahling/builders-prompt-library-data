---
title: "Dockerize a Node.js Application"
slug: dockerize-a-node-js-application
stage: Ship
category: "Deployment & Launch"
grade: A
score: 87
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/dockerize-a-node-js-application
---
# Dockerize a Node.js Application

Containerize a Node.js REST API using a multi-stage Dockerfile based on Alpine Linux to ensure a lightweight and production-ready deployment.

Variables: port_number

## Prompt

You are a software developer. Your task is to dockerize a Node.js application. The application is a simple REST API with a `package.json` file defining its dependencies.

Instructions:
1. Write a `Dockerfile` that starts from a `node:18-alpine` base image.
2. Copy the `package.json` and `package-lock.json` files and install dependencies using `npm install`.
3. Copy the rest of the application code into the container.
4. Expose port {{port_number}} and define the command to start the application.

## Tips

A great starting point for learning how to containerize applications with Docker.
