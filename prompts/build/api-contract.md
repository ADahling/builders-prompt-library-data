---
title: "Generate an API contract"
slug: api-contract
stage: Build
category: "API Design"
grade: A+
score: 93
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/api-contract
---
# Generate an API contract

Write an API contract in OpenAPI-style Markdown with schemas, JSON examples, error criteria, and access rules matching existing REST conventions.

Variables: capability

## Prompt

You are an API designer. Your task is: write the API contract for {{capability}} against the current stack and its existing REST conventions.

1. Cover endpoints, methods, authentication, authorization, request and response schemas, validation, pagination, idempotency, rate limits, error codes, and example payloads.
2. For each endpoint, give every request schema one valid example and every documented error code one example error body.

Output format: OpenAPI-style Markdown. Example payloads must be complete JSON that parses as-is: never use ellipses, comments, placeholders, or abbreviated arrays and objects. Fence pure JSON as ```json; fence HTTP exchanges, request or status line plus headers and body, as ```http.

State validation rules and error codes as pass/fail acceptance criteria per field, and flag any endpoint whose behavior you had to assume.

Give a full response schema for every endpoint, including list and collection responses. Give one example error body for every validation detail code you define. Only call something an existing convention if the inputs show it; otherwise mark it Assumed. For tokens or secrets, state how they are generated, stored and compared, and how replays of the same idempotency key behave.

If the full result does not fit in one reply, deliver it in parts in the order above, finish each part completely, and stop after each part so I can say continue. Never abbreviate required examples or omit controls to fit the reply.

## Tips

Runtime verification showed the original version mislabeled HTTP exchanges and abbreviated arrays as JSON. The fence-label, no-ellipsis, and full-expansion rules exist so every payload can be copied straight into a parser or test fixture.
