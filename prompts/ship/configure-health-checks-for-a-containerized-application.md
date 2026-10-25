---
title: "Configure Health Checks for a Containerized Application"
slug: configure-health-checks-for-a-containerized-application
stage: Ship
category: "Deployment & Launch"
grade: B
score: 72
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/configure-health-checks-for-a-containerized-application
---
# Configure Health Checks for a Containerized Application

Configure liveness and readiness probes to automate failure recovery and traffic routing for orchestrated containerized applications.

Variables: container_orchestrator

## Prompt

You are a DevOps engineer. Your task is to configure health checks for a containerized application running in `{{container_orchestrator}}`.

Instructions:
1. Implement a `liveness` probe to restart the container if it becomes unresponsive.
2. Implement a `readiness` probe to ensure the container only receives traffic when it's ready.
3. Choose appropriate health check mechanisms (e.g., HTTP endpoint, TCP socket, command execution).
4. Set appropriate initial delays, periods, and timeouts for the probes.

## Tips

Essential for building resilient and self-healing systems with containers.
