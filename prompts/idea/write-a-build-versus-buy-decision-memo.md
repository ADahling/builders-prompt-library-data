---
title: "Write a build versus buy decision memo"
slug: write-a-build-versus-buy-decision-memo
stage: Idea
category: "Business & Strategy"
grade: A
score: 80
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/write-a-build-versus-buy-decision-memo
---
# Write a build versus buy decision memo

Compare building a capability against buying it, including exit cost and the maintenance tail.

Variables: capability, candidate_vendor

## Prompt

You are a technical decision maker writing a memo on whether to build or buy a capability.

Context:
- The capability: {{capability}}
- The vendor under consideration: {{candidate_vendor}}

Your task is to produce a memo that survives scrutiny from both engineering and finance.

Steps:
1. State the decision, the deadline, and who owns it, in three sentences at the top.
2. Define what the capability must do, split into must-have and nice-to-have, with the source of each requirement.
3. Cost the build over three years: initial delivery, maintenance, on-call load, and opportunity cost.
4. Cost the buy over three years: licence, integration, per-unit scaling, and the work that remains in-house.
5. Assess lock-in: data portability, contractual exit terms, and the cost of migrating away in year three.
6. Give the recommendation, the two strongest arguments against it, and the trigger that would reverse it.

Constraints:
- Do not treat engineering time as free in either column.
- Do not compare a full vendor product against a minimal build; scope both to the must-haves.
- Flag every cost you had to assume, and mark it as an assumption.

Output format, in Markdown: a **Decision** block, a requirements table with columns requirement, priority, source, a three-year cost table with columns year, build, buy, then **Lock-in**, **Recommendation**, **Strongest objections**, and **Reversal trigger**.

## Tips

Price the maintenance tail and the exit. Build-versus-buy decisions go wrong on year three, not month one.
