---
title: "Fixing a Critical Bug in a Payment Processing Retry Logic"
slug: fixing-a-critical-bug-in-a-payment-processing-retry-logic
stage: Test
category: "Critical Bugs"
grade: A
score: 87
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/fixing-a-critical-bug-in-a-payment-processing-retry-logic
---
# Fixing a Critical Bug in a Payment Processing Retry Logic

Plan triage for duplicate payment charges with a kill switch, detection queries, refunds, and analysis of unsafe retry logic.

Variables: app_name

## Prompt

Our {{app_name}} application has a background job that retries failed customer payments. A critical bug has been discovered in this retry logic: under certain conditions, it is retrying non-idempotent payment API calls, resulting in some customers being charged multiple times for the same invoice. This is a major customer trust and financial issue.

As the senior engineer responsible for the billing system, you need to stop the bleeding, fix the bug, and redesign the retry logic to be safe and idempotent.

1.  **Immediate Triage and Damage Control:**
    *   What is the first action you take to stop the multiple charges? (Hint: It involves a kill switch).
    *   How do you identify all the customers who have been incorrectly charged multiple times? Provide the SQL or database query logic you would use to find these duplicate charges.
    *   What is the plan for communicating with the affected customers and processing refunds? This is a customer trust issue, so the response must be swift and transparent.

2.  **Root Cause Analysis of the Bug:**
    *   The bug is in the retry logic. The code catches any exception from the payment gateway API call and schedules a retry. Why is this naive approach so dangerous?
    *   Explain the concept of **idempotency** in the context of API calls. Why is it critical for payment processing?
    *   Differentiate between the types of errors a payment gateway can return. Which errors are safe to retry, and which are not?
        *   **Safe to retry:** Network timeouts, API rate limiting (e.g., HTTP 429), server-side errors (HTTP 5xx).
        *   **Unsafe to retry:** Successful but declined payments (e.g., insufficient funds), payments that have already been processed, invalid card details.

3.  **Designing a Safe Retry Logic:**
    *   Design and provide pseudocode for a new, safer retry worker.
    *   Your new logic must inspect the error returned from the payment gateway *before* deciding to retry. It should only retry on specific, transient, and idempotent-safe error codes.
    *   Your logic should implement an exponential backoff strategy. Explain what this is and why it's important for retry logic.
    *   Your logic must have a maximum retry limit. After a certain number of retries, it should give up and flag the payment for manual review.

4.  **Leveraging Idempotency Keys:**
    *   Even with safer retry logic, network issues can leave you in an unknown state. The best solution is to use idempotency keys. 
    *   Explain what an idempotency key is (e.g., the 'Idempotency-Key' HTTP header used by Stripe and other gateways).
    *   Show how to modify your payment processing code to generate a unique idempotency key for each transaction attempt and include it in the API request.
    *   Explain how this key prevents duplicate charges even if the same request is sent multiple times.

5.  **Testing and Validation:**
    *   How would you test your new, safe retry logic? You can't use real credit cards.
    *   Describe how to use the payment gateway's sandbox environment and special test card numbers or tokens that can simulate specific failure scenarios (e.g., a card that always times out, a card that is always declined).
    *   What kind of integration tests would you write to ensure your retry logic behaves correctly under these different failure modes?

Your response should be a detailed engineering plan of at least 600 words, focusing on robust, fault-tolerant system design.
