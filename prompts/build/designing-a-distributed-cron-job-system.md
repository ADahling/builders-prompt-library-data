---
title: "Designing a Distributed Cron Job System"
slug: designing-a-distributed-cron-job-system
stage: Build
category: "System Architecture"
grade: A
score: 82
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/designing-a-distributed-cron-job-system
---
# Designing a Distributed Cron Job System

Design a resilient, high-scale distributed cron system using leader election, message queues, and worker pools to ensure reliable task execution.

## Prompt

You are a platform engineer at a large company. Your teams need a reliable and scalable way to run scheduled tasks (cron jobs). The standard cron on a single server is not fault-tolerant and doesn't scale.

**Your Task:**
Design a distributed, fault-tolerant cron job system.

**Instructions & Constraints:**
1.  **Requirements:**
    *   **Reliability:** A job should be executed at least once. Ideally, exactly once.
    *   **Scalability:** The system should be able to handle thousands of scheduled jobs.
    *   **Fault Tolerance:** If the node that is supposed to run a job fails, another node should take over.
    *   **Observability:** We need to be able to see the status of jobs (scheduled, running, succeeded, failed).

2.  **High-Level Architecture:**
    *   Propose a high-level architecture with the following components:
        *   **Job Store:** A database to store the definitions of all the jobs (e.g., the schedule, the command to run).
        *   **Scheduler:** A component that is responsible for figuring out which jobs need to run now.
        *   **Executor:** A pool of workers that actually execute the jobs.

3.  **The Scheduler (The Hard Part):**
    *   The scheduler needs to be fault-tolerant. This is a classic use case for **leader election**.
    *   Design the scheduler component:
        1.  Multiple instances of the scheduler run, but only one is the active leader at any given time.
        2.  The leader periodically scans the Job Store for jobs that are due to run.
        3.  When a job is due, the leader puts a "run job" message onto a message queue.
        4.  The leader needs to use locking to ensure that it doesn't schedule the same job twice.

4.  **The Executors:**
    *   The executors are a pool of stateless workers that listen to the message queue.
    *   When a worker receives a "run job" message, it executes the job.
    *   After the job is done, the worker updates the status of the job in the Job Store.

5.  **Technology Choices:**
    *   Recommend a technology stack for this system:
        *   **Job Store:** A relational database like PostgreSQL.
        *   **Leader Election for Scheduler:** Use a coordination service like ZooKeeper or etcd.
        *   **Message Queue:** RabbitMQ or SQS.

6.  **Ensuring "Exactly Once" Execution:**
    *   Discuss the challenges of achieving exactly-once execution and how to get close to it (e.g., by having the executor acquire a lock before running the job).

**Output Format:**
Generate a detailed design document in Markdown:
1.  **The Need for a Distributed Cron System**
2.  **High-Level Architecture**
3.  **Designing a Fault-Tolerant Scheduler with Leader Election**
4.  **The Executor Pool: A Scalable Workforce**
5.  **Our Recommended Technology Stack**
6.  **The Quest for Exactly-Once Execution**
