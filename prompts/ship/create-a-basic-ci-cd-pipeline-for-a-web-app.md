---
title: "Create a Basic CI/CD Pipeline for a Web App"
slug: create-a-basic-ci-cd-pipeline-for-a-web-app
stage: Ship
category: "Deployment & Launch"
grade: B
score: 79
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-basic-ci-cd-pipeline-for-a-web-app
---
# Create a Basic CI/CD Pipeline for a Web App

Automate a multi-stage CI/CD pipeline that builds, tests, and provides status notifications for full-stack web applications.

Variables: ci_cd_tool, frontend_framework, backend_framework, notification_channel

## Prompt

You are a DevOps engineer. Your task is to create a basic CI/CD pipeline for a simple web application using {{ci_cd_tool}}. The application consists of a frontend built with {{frontend_framework}} and a backend API using {{backend_framework}}.

Instructions:
1. Configure the pipeline to trigger on every push to the `main` branch.
2. Include stages for building the frontend and backend code.
3. Add a stage for running unit tests for both frontend and backend.
4. Ensure the pipeline notifies the team on {{notification_channel}} upon success or failure.

## Tips

This prompt is ideal for developers new to CI/CD, providing a foundational understanding of pipeline automation.
