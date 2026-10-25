---
title: "Create a Chaos Engineering Experiment to Test the Resilience of a System"
slug: create-a-chaos-engineering-experiment-to-test-the-resilience-of-a-system
stage: Build
category: "Backend & Data Integrity"
grade: B
score: 74
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-a-chaos-engineering-experiment-to-test-the-resilience-of-a-system
---
# Create a Chaos Engineering Experiment to Test the Resilience of a System

Design a failure-injection experiment to assess system resilience, with a hypothesis, scope, metrics, rollback steps, and team communication.

Variables: system_name

## Prompt

I want to test the resilience of our {{system_name}} system by intentionally injecting failures into it. This will help us to identify weaknesses in our system and to improve its fault tolerance. I need to create a chaos engineering experiment.

Your task is to design a chaos engineering experiment. The design should include:

1.  **Hypothesis:** A clear hypothesis about how the system will behave when a failure is injected. For example, "If we shut down one of the web servers, the load balancer will redirect the traffic to the remaining servers, and users will not experience any downtime."
2.  **Experiment Design:** A detailed design for the experiment. This should include the type of failure to inject (e.g., shutting down a server, introducing network latency), the scope of the experiment (e.g., which servers to target), and the duration of the experiment.
3.  **Metrics:** A list of the metrics to measure during the experiment to determine its impact. This should include both system-level metrics (e.g., CPU utilization, error rates) and business-level metrics (e.g., number of successful transactions).
4.  **Rollback Plan:** A plan for how to quickly stop the experiment and to roll back any changes if it causes a problem.
5.  **Communication Plan:** A plan for how to communicate the experiment to the rest of the team to avoid any confusion or panic.

## Tips

This prompt is for organizations that are serious about building resilient and fault-tolerant systems.
