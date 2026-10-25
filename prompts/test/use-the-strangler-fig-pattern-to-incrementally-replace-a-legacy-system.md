---
title: "Use the Strangler Fig Pattern to Incrementally Replace a Legacy System"
slug: use-the-strangler-fig-pattern-to-incrementally-replace-a-legacy-system
stage: Test
category: "Cleanup & Warnings"
grade: A
score: 87
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/use-the-strangler-fig-pattern-to-incrementally-replace-a-legacy-system
---
# Use the Strangler Fig Pattern to Incrementally Replace a Legacy System

Plan an incremental legacy migration with the Strangler Fig pattern, facade routing, feature prioritization, and microservice implementation.

Variables: legacy_tech_stack, modern_tech_stack, legacy_system_functionalities, api_gateway_name

## Prompt

My company has a large, monolithic legacy system written in `{{legacy_tech_stack}}`. We want to replace it with a new system built with modern microservices using `{{modern_tech_stack}}`. A "big bang" rewrite is too risky and would take too long.

I have read about the "Strangler Fig Pattern" as a way to do this incrementally and safely. Your task is to create a detailed architectural plan for applying this pattern to our system.

Our legacy system has the following key functionalities: `{{legacy_system_functionalities}}`.

1.  **The Strangler Fig Pattern Explained:** Start with a clear explanation of the pattern. Use the metaphor of the strangler fig vine gradually taking over a host tree.
2.  **The Facade:** The first step is to put a facade in front of the legacy system. What technology should we use for this facade? An API Gateway like `{{api_gateway_name}}`? A reverse proxy like Nginx? Propose a solution and explain how it would route traffic.
3.  **First Feature to Strangle:** How do we choose the first piece of functionality to "strangle" (i.e., to reimplement in the new system)? Propose a prioritization framework. Should we start with something easy, or something that provides high business value?
4.  **Implementation Plan:** Provide a step-by-step plan for strangling one specific feature. This should cover:
    *   Developing the new microservice for that feature.
    *   Updating the facade to route traffic for that feature to the new service, while all other traffic continues to go to the legacy system.
    *   Handling data synchronization between the new service and the legacy database. What is the "data synchronization" or "data migration" strategy?
5.  **Repeating the Process:** Explain how this process is repeated for each feature until the entire legacy system is "strangled" and can be decommissioned.

Output should be a high-level architectural strategy document.

## Tips

The Strangler Fig Pattern is the industry-standard and safest way to deal with the monumental task of replacing a legacy system.
