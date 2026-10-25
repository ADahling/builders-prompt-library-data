---
title: "Design a Circuit Breaker for a Resilient Microservice Architecture"
slug: design-a-circuit-breaker-for-a-resilient-microservice-architecture
stage: Build
category: "API Design"
grade: A
score: 80
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/design-a-circuit-breaker-for-a-resilient-microservice-architecture
---
# Design a Circuit Breaker for a Resilient Microservice Architecture

Design a resilient microservice architecture by implementing a state-managed circuit breaker pattern to prevent cascading system failures.

## Prompt

I am building a microservices-based application where services often call each other. I need to implement a circuit breaker pattern to prevent a single service failure from cascading and taking down the entire application.

Your task is to design a circuit breaker component.

**Instructions:**
1.  **Circuit Breaker States:** Describe the three states of a circuit breaker: Closed, Open, and Half-Open.
2.  **State Transitions:** Explain the conditions under which the circuit breaker transitions from one state to another. For example, when does it trip from Closed to Open? When does it switch from Open to Half-Open?
3.  **Implementation:** Provide a pseudo-code example of a circuit breaker implementation in a language of your choice. The example should show how to wrap a remote call in a circuit breaker.

**Output Format:**
Provide the output as a Markdown document. First, explain the three states of the circuit breaker. Then, describe the state transitions with a state diagram. Finally, provide the pseudo-code example.
