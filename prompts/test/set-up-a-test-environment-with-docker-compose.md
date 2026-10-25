---
title: "Set Up a Test Environment with Docker Compose"
slug: set-up-a-test-environment-with-docker-compose
stage: Test
category: "Testing & QA"
grade: A
score: 83
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/set-up-a-test-environment-with-docker-compose
---
# Set Up a Test Environment with Docker Compose

Generate a Docker Compose configuration and orchestration scripts to automate the deployment and teardown of a multi-service test environment.

Variables: service_1, service_2, database

## Prompt

You are a junior DevOps engineer. Your task is to set up a test environment with Docker Compose for a multi-service application. The application consists of a {{service_1}}, a {{service_2}}, and a {{database}}.

Context:
- You need to create a Docker Compose file that defines the services and their dependencies.
- The test environment should be easy to start and stop with a single command.

Provide:
1. A `docker-compose.yml` file that defines the services and their configurations.
2. A script to start the test environment in the background.
3. A script to stop the test environment and remove the containers.

## Tips

A beginner-friendly prompt for learning how to use Docker Compose to create isolated and reproducible test environments.
