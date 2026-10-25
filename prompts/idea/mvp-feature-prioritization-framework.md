---
title: "MVP Feature Prioritization Framework"
slug: mvp-feature-prioritization-framework
stage: Idea
category: "Idea to PRD"
grade: A
score: 82
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/mvp-feature-prioritization-framework
---
# MVP Feature Prioritization Framework

Analyze and rank product features using RICE, MoSCoW, and Kano models to define a lean MVP scope, roadmap, and core success metrics.

Variables: product_name, product_description, feature_list

## Prompt

You are a product manager. Help me prioritize features for the MVP of {{product_name}}, a {{product_description}}.

Proposed features:
{{feature_list}}

Apply these prioritization frameworks:

1. **RICE Scoring**: Score each feature on Reach, Impact, Confidence, Effort
2. **MoSCoW Method**: Categorize as Must-have, Should-have, Could-have, Won't-have
3. **Kano Model**: Classify as Basic, Performance, or Delight features
4. **Value vs Effort Matrix**: Plot each feature on a 2x2 matrix

Then provide:
5. **MVP Feature Set**: The minimum set of features for a viable product
6. **V1.1 Roadmap**: What to add in the first update
7. **Cut List**: Features to explicitly NOT build (with reasons)
8. **Dependencies**: Feature dependency graph (what must be built first)
9. **Success Metrics**: How to measure if each feature is working

Be ruthless about cutting. The best MVPs do one thing exceptionally well.

## Tips

The hardest part of product management is saying no. This framework makes it systematic.
