---
title: "MVP Scope Negotiation Framework"
slug: mvp-scope-negotiation-framework
stage: Idea
category: "Idea to PRD"
grade: B
score: 78
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/mvp-scope-negotiation-framework
---
# MVP Scope Negotiation Framework

Ruthlessly scope an MVP: brainstorm every feature, sort them into ships-now versus later, and defend the cut list.

## Prompt

I want to build [describe app]. Help me ruthlessly scope the MVP:

1. Feature Brainstorm: List every feature you can think of for this product (aim for 20+).
2. Categorize each feature:
   - Core (app is broken without this)
   - Important (users expect it, but can launch without)
   - Nice-to-have (adds polish, not essential)
   - Future (v2 or later)
3. The "One Thing" Test: What is the ONE workflow that must work flawlessly on day one? Describe it step-by-step.
4. Cut List: Features that feel core but can actually be faked, hardcoded, or done manually at launch (e.g., admin panel = spreadsheet, notifications = manual email, onboarding = Loom video).
5. MVP Timeline: Estimate build time for Core features only. If more than 2 weeks of dev time, cut more.
6. Launch Criteria: 5 specific, testable statements that must be true before you launch.

Goal: Ship in 1-2 weeks, not 2 months.

## Tips

The hardest part of building is deciding what NOT to build. Use this to stay focused.
