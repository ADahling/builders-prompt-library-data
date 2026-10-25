---
title: "Advanced Debugging Strategy"
slug: advanced-debugging-strategy
stage: Test
category: "Testing & QA"
grade: A
score: 86
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/advanced-debugging-strategy
---
# Advanced Debugging Strategy

Get likely root causes, diagnostic steps, and targeted fixes for an app issue using your symptoms, logs, code, and prior investigation.

## Prompt

I'm debugging an issue with the following characteristics:

SYMPTOMS:
- [Describe the observable problem in detail, e.g., "React component re-renders infinitely"]
- Occurs approximately [FREQUENCY] under [SPECIFIC CONDITIONS]
- Started after [RELEVANT CHANGE, DEPLOYMENT, OR TIMELINE]

ENVIRONMENT:
- Technologies and versions: [React 18, Node 20, PostgreSQL]
- Hosting/infra: [cloud provider, container/orchestration, etc.]
- Relevant configuration details: [feature flags, env vars, etc.]

INVESTIGATION SO FAR:
- Steps already taken: [Step 1, Step 2]
- Evidence collected: [Logs, metrics, screenshots]
- Theories explored and ruled out: [Theory + why it's unlikely]

ERROR LOGS:
[Include relevant logs here]

RELEVANT CODE:
[Include suspicious code sections, e.g., custom hooks, middleware]

Help me by:
1. Suggesting the most likely root causes based on this information
2. Proposing specific diagnostic steps to confirm or rule out each hypothesis
3. Recommending targeted fixes or refactors once the cause is identified

## Tips

Structured debugging prevents the common mistake of trying random fixes. Source: medium.com/@onix_react/ultimate-prompts-for-every-developer
