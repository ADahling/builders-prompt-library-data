---
title: "Create a Kubernetes Deployment for a Microservice"
slug: create-a-kubernetes-deployment-for-a-microservice
stage: Ship
category: "Deployment & Launch"
grade: A
score: 84
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-kubernetes-deployment-for-a-microservice
---
# Create a Kubernetes Deployment for a Microservice

Generate a production-ready Kubernetes Deployment YAML with defined replicas, resource constraints, and health checks for a microservice.

Variables: docker_image_name

## Prompt

You are a cloud engineer. Your task is to create a Kubernetes Deployment to manage a microservice. The microservice is packaged as a Docker image, `{{docker_image_name}}`.

Instructions:
1. Write a YAML file for a Deployment object.
2. Specify the Docker image and the number of replicas (e.g., 3).
3. Define resource requests and limits for CPU and memory.
4. Add readiness and liveness probes to ensure the service is healthy.

## Tips

Introduces the fundamental Kubernetes object for deploying and scaling applications.
