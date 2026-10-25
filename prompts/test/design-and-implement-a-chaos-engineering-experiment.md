---
title: "Design and Implement a Chaos Engineering Experiment"
slug: design-and-implement-a-chaos-engineering-experiment
stage: Test
category: "Testing & QA"
grade: A
score: 80
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-and-implement-a-chaos-engineering-experiment
---
# Design and Implement a Chaos Engineering Experiment

Design and execute structured chaos engineering experiments to identify architectural weaknesses and validate system resilience against failures.

Variables: system_type, chaos_engineering_tool

## Prompt

You are a reliability engineer. Your task is to design and implement a chaos engineering experiment to test the resilience of a distributed system. The system is a {{system_type}} that is designed to be fault-tolerant.

Context:
- You want to proactively identify weaknesses in the system by injecting failures in a controlled environment.
- You will use a chaos engineering tool like {{chaos_engineering_tool}}.

Provide:
1. A hypothesis for the chaos engineering experiment.
2. A plan for injecting a specific failure into the system (e.g., network latency, pod failure).
3. A set of metrics to measure the impact of the failure and the system's ability to recover.

## Tips

An advanced prompt for reliability engineers who want to practice chaos engineering to build more resilient systems.
