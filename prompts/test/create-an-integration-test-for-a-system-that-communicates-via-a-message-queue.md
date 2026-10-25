---
title: "Create an Integration Test for a System that Communicates via a Message Queue"
slug: create-an-integration-test-for-a-system-that-communicates-via-a-message-queue
stage: Test
category: "Testing & QA"
grade: C
score: 64
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/create-an-integration-test-for-a-system-that-communicates-via-a-message-queue
---
# Create an Integration Test for a System that Communicates via a Message Queue

Generate an end-to-end integration test and validation script to verify message delivery and processing between a producer and consumer.

Variables: message_queue_provider

## Prompt

You are a software engineer working on a distributed system. Your task is to create an integration test for a system that communicates via a message queue. The system consists of a producer that sends messages to the queue and a consumer that receives messages from the queue.

Context:
- You need to test that the messages are sent and received correctly and that the system behaves as expected.
- You will use a real message queue, such as {{message_queue_provider}}, in your test environment.

Provide:
1. An integration test that starts the producer and the consumer.
2. A script to send a message to the message queue.
3. Assertions to verify that the consumer receives the message and processes it correctly.

## Tips

A prompt for engineers who are building distributed systems with message queues and need to test their integration.
