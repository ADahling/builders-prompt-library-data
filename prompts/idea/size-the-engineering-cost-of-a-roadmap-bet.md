---
title: "Size the engineering cost of a roadmap bet"
slug: size-the-engineering-cost-of-a-roadmap-bet
stage: Idea
category: "Business & Strategy"
grade: A
score: 82
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/size-the-engineering-cost-of-a-roadmap-bet
---
# Size the engineering cost of a roadmap bet

Turn a proposed feature into a defensible range of engineering cost with the assumptions made explicit.

Variables: feature_description, team_shape

## Prompt

You are an engineering lead sizing a proposed roadmap item before it is committed.

Context:
- The proposal: {{feature_description}}
- The team available: {{team_shape}}

Your task is to produce a cost range a product leader can plan against, with the uncertainty visible.

Steps:
1. Decompose the proposal into deliverable slices, each independently shippable, and describe each in one line.
2. For each slice, give an optimistic and a pessimistic estimate in engineer-weeks, and name the assumption that separates them.
3. Identify the work that is not feature code: migrations, backfills, instrumentation, documentation, and rollout.
4. List the dependencies outside the team and what happens to the estimate if each slips.
5. Name the three unknowns that most affect the total, and propose a time-boxed spike for each.
6. Give the total range, the confidence level, and the smallest version that delivers most of the value.

Constraints:
- Do not produce a single point estimate.
- Do not omit rollout, testing, or migration work from the total.
- Keep every estimate traceable to a named slice.

Output format, in Markdown: a slices table with columns slice, optimistic, pessimistic, key assumption; then **Non-feature work**, **Dependencies**, **Spikes**, and a **Bottom line** paragraph with the range and confidence.

## Tips

Ranges with named assumptions beat point estimates. State what would move the number, and by how much.
