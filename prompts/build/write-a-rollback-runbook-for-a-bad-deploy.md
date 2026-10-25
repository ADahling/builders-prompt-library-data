---
title: "Write a rollback runbook for a bad deploy"
slug: write-a-rollback-runbook-for-a-bad-deploy
stage: Build
category: "DevOps & IaC"
grade: A
score: 80
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-a-rollback-runbook-for-a-bad-deploy
---
# Write a rollback runbook for a bad deploy

Produce a step-by-step rollback procedure with decision points, data considerations, and verification.

Variables: service_name, deploy_mechanism

## Prompt

You are an on-call engineer writing the rollback runbook for a service.

Context:
- The service: {{service_name}}
- How it deploys: {{deploy_mechanism}}

Your task is to write a procedure someone unfamiliar with the service can execute correctly at 3am.

Steps:
1. State the decision criteria: the observable signals that justify a rollback, and the ones that do not.
2. Write the rollback procedure as numbered commands, each with the expected output and the check that it worked.
3. Handle data: state which migrations are reversible, which are not, and the procedure for the forward-only case.
4. Define the verification sequence after rollback: health checks, key user path, and the metrics that must return to baseline.
5. Define the communication steps: who is told, in what channel, with what template.
6. List the follow-up actions required before the next deploy attempt.

Constraints:
- Every command must be copy-pasteable and name the environment explicitly.
- Never instruct an operator to delete data as part of a rollback.
- If a step cannot be automated, say why in one line.

Output format, in Markdown: **Rollback if / do not roll back if** as two lists, then a numbered **Procedure** with a command block and expected output per step, then **Verification**, **Comms**, and **Follow-ups**.

## Tips

Write the runbook while the deploy is calm. The person who reads it will be tired and under pressure.
