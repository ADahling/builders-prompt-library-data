---
title: "Troubleshoot a Distributed System 'Gray Failure'"
slug: troubleshoot-a-distributed-system-gray-failure
stage: Test
category: "Critical Bugs"
grade: B
score: 78
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/troubleshoot-a-distributed-system-gray-failure
---
# Troubleshoot a Distributed System 'Gray Failure'

Design robust health checks to detect and mitigate gray failures by verifying dependency connectivity and service responsiveness.

## Prompt

You are a senior SRE. A service in your distributed system is experiencing a 'gray failure'. It is not completely down, but it is responding very slowly or with a high error rate, and it is not being detected by your health checks. This is impacting the overall system performance. Your task is to improve the health checking to detect such failures.

Context:
- The current health check is a simple TCP check on the service's port, which succeeds even if the service is unhealthy.
- The service has dependencies on a database and another downstream service.
- A failure in the database is causing the service to perform poorly, but not to crash.

Provide:
1. An explanation of what a gray failure is and why it is difficult to detect.
2. A design for a more comprehensive health check endpoint (e.g., `/healthz`) for the service. This endpoint should not just check if the process is running, but also check its ability to connect to its dependencies (like the database) and perform a trivial operation.
3. A strategy for how the load balancer or service orchestrator (like Kubernetes) should use this improved health check to stop sending traffic to unhealthy instances and restart them.

## Tips

Addresses a subtle but important aspect of building robust, self-healing distributed systems.
