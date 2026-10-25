---
title: "Deploy a Multi-Container Application with Docker Compose"
slug: deploy-a-multi-container-application-with-docker-compose
stage: Ship
category: "Deployment & Launch"
grade: B
score: 76
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/deploy-a-multi-container-application-with-docker-compose
---
# Deploy a Multi-Container Application with Docker Compose

Orchestrate a multi-container architecture by configuring a Docker Compose file with service networking and persistent data volumes.

Variables: database_image, cache_image

## Prompt

You are a backend developer. Your task is to use Docker Compose to define and run a multi-container application. The application consists of a web server, a database, and a caching layer.

Instructions:
1. Write a `docker-compose.yml` file to define the three services: `web`, `db`, and `cache`.
2. Use official images from Docker Hub for the database (`{{database_image}}`) and cache (`{{cache_image}}`).
3. Configure networking so that the services can communicate with each other.
4. Define volumes to persist the database data.

## Tips

A practical exercise for managing the complexity of microservices-based applications locally.
