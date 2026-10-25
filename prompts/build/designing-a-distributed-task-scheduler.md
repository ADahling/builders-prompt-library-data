---
title: "Designing a Distributed Task Scheduler"
slug: designing-a-distributed-task-scheduler
stage: Build
category: "System Architecture"
grade: B
score: 72
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/designing-a-distributed-task-scheduler
---
# Designing a Distributed Task Scheduler

Design a fault-tolerant, two-level distributed task scheduler for large-scale data processing using DAGs and leader election.

## Prompt

You are a software architect designing a distributed task scheduler for a large-scale data processing system. The scheduler needs to be able to manage thousands of tasks across a cluster of hundreds of machines.

**Your Task:**
Design a fault-tolerant and scalable distributed task scheduler.

**Instructions & Constraints:**
1.  **Requirements:**
    *   Users can submit complex workflows (DAGs of tasks).
    *   The scheduler must be fault-tolerant. If the scheduler fails, another one should take over.
    *   The scheduler must be scalable to handle a large number of tasks and workers.

2.  **Architecture:**
    *   Propose a two-level scheduling architecture (like Apache Mesos or Kubernetes):
        *   **Central Scheduler:** Responsible for high-level scheduling decisions (e.g., which tasks to run, resource allocation).
        *   **Worker-Side Schedulers (Executors):** Responsible for the actual execution of tasks on the worker nodes.

3.  **Fault Tolerance:**
    *   The central scheduler is a critical component. Explain how you would make it fault-tolerant using leader election.

4.  **Resource Management:**
    *   Describe how the scheduler will manage resources (CPU, memory) across the cluster.

5.  **Task Execution:**
    *   Explain how tasks are launched and monitored on the worker nodes.

**Output Format:**
Generate a design document in Markdown:
1.  **Designing a Scalable and Resilient Task Scheduler**
2.  **A Two-Level Scheduling Architecture**
3.  **Ensuring Fault Tolerance with Leader Election**
4.  **Resource Management and Task Execution**
