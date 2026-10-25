---
title: "Debug a Failure in a Distributed Transaction"
slug: debug-a-failure-in-a-distributed-transaction
stage: Test
category: "Critical Bugs"
grade: C
score: 65
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/debug-a-failure-in-a-distributed-transaction
---
# Debug a Failure in a Distributed Transaction

Design a resilient Saga-based architecture for distributed transactions to resolve consistency failures and implement robust error compensation.

## Prompt

You are a senior engineer working on an e-commerce platform. The order processing workflow involves a distributed transaction that spans multiple microservices (e.g., Order Service, Payment Service, Inventory Service). The transaction is failing intermittently, leaving the system in an inconsistent state (e.g., payment taken but inventory not updated). Your task is to design a more robust solution.

Context:
- The current implementation is trying to use a two-phase commit (2PC) protocol, but it's complex and unreliable.
- The services communicate over a message bus (like RabbitMQ).
- When a failure occurs, it's difficult to know which part of the transaction failed.

Provide:
1. An explanation of the challenges of distributed transactions and the pitfalls of two-phase commit.
2. A design for a more resilient solution using the Saga pattern. Describe the sequence of local transactions and the compensating transactions that would be used to roll back the changes in case of a failure.
3. A discussion on the importance of idempotency in the design of the services participating in the saga.

## Tips

A complex architectural problem that requires knowledge of advanced distributed systems patterns.
