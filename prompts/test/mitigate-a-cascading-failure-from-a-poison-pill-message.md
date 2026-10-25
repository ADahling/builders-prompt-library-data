---
title: "Mitigate a Cascading Failure from a Poison Pill Message"
slug: mitigate-a-cascading-failure-from-a-poison-pill-message
stage: Test
category: "Critical Bugs"
grade: B
score: 74
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/mitigate-a-cascading-failure-from-a-poison-pill-message
---
# Mitigate a Cascading Failure from a Poison Pill Message

Implement a dead-letter queue strategy to isolate malformed messages and prevent consumer crash loops in distributed messaging systems.

## Prompt

You are a distributed systems developer. You have a system where services communicate via a message queue. A malformed message (a ‘poison pill’) has been sent to a queue. Any consumer that tries to process this message crashes. Because the message is not acknowledged, it is returned to the queue, and the next consumer that picks it up also crashes. This leads to a cycle of consumer crashes.

Context:
- The system uses a message queue like RabbitMQ or AWS SQS.
- The message is malformed in a way that the deserialization logic in the consumer throws an unhandled exception.
- The consumers are in a crash loop.

Provide:
1. An explanation of the poison pill problem.
2. A solution that involves implementing a dead-letter queue (DLQ). After a consumer fails to process a message a certain number of times (e.g., 3 times), the message queue should automatically move the message to the DLQ instead of returning it to the main queue. This isolates the poison pill and allows the consumers to continue processing valid messages.
3. A plan for how to handle the messages in the DLQ. This would involve setting up monitoring and alerting on the DLQ, and having a process to manually inspect the poison pill messages to debug the root cause.

## Tips

A classic failure mode in message-driven architectures.
