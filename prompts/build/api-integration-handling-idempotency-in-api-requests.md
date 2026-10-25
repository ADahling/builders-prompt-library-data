---
title: "API Integration: Handling Idempotency in API Requests"
slug: api-integration-handling-idempotency-in-api-requests
stage: Build
category: "LLM & AI Integration"
grade: A
score: 85
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/api-integration-handling-idempotency-in-api-requests
---
# API Integration: Handling Idempotency in API Requests

Implement idempotent payment processing in Python using unique header keys and the requests library to prevent duplicate transactions during retries.

## Prompt

As a senior backend developer, you are designing an API that processes payments. It is absolutely critical that if a client sends the same request twice due to a network error, they are not charged twice. This property is called 'idempotency'.

Your task is to write a Python script demonstrating how to handle idempotency in an API client by using an `Idempotency-Key`.

**Scenario:**
- You are calling a fictional payment API.
- To ensure idempotency, the API requires you to send a unique key in the `Idempotency-Key` header for each transaction. If you send a request with a key that the server has already processed, the server will not perform the action again but will simply return the original result.

**Technical Requirements:**
- Use the 'requests' and 'uuid' libraries.
- **Step 1:** Create a function `make_payment(amount, idempotency_key)`.
    -   This function should print the idempotency key it is using.
    -   It should make a POST request to a mock API endpoint (e.g., `http://httpbin.org/post`).
    -   It must include the `Idempotency-Key` in the request headers.
    -   It should send the `amount` in the JSON body.
- **Step 2:** Demonstrate the workflow.
    -   Generate a unique idempotency key for a new transaction using `str(uuid.uuid4())`.
    -   Call `make_payment` for the first time with an amount of $100 and the new key. Print the (mock) response.
    -   Simulate a client-side retry due to a network error: Call `make_payment` *again* with the *exact same* idempotency key and amount.
    -   Explain in a comment that a real idempotent API would recognize the second key and return the original successful response without creating a second charge.
- **Step 3:** Show a new transaction.
    -   Generate a *new* idempotency key.
    -   Call `make_payment` with this new key to show how a separate transaction would be processed.

**Output Format:**
A complete, executable Python script with comments explaining the concept and the workflow.
