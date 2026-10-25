---
title: "Rewrite a landing page hero around one claim"
slug: rewrite-a-landing-page-hero-around-one-claim
stage: Design
category: "Landing Page & Marketing"
grade: B
score: 74
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/rewrite-a-landing-page-hero-around-one-claim
---
# Rewrite a landing page hero around one claim

Cut a hero section to a single verifiable claim, a concrete subhead, and one primary action.

Variables: current_hero, product_truth

## Prompt

You are a product marketer rewriting a hero section that says too much and proves nothing.

Context:
- The current hero copy: {{current_hero}}
- What the product actually does, in plain terms: {{product_truth}}

Your task is to rewrite the hero around a single claim you can substantiate on the same page.

Steps:
1. Extract every claim the current hero makes. Mark each as provable, vague, or unsupportable.
2. Choose the one claim that is both provable and the reason a visitor would stay. Justify the choice in one line.
3. Write the headline stating that claim in under twelve words, with no buzzwords and no metaphor.
4. Write a subhead of one or two sentences naming who it is for and what changes for them.
5. Write one primary call to action, and at most one secondary. Both must describe the action, not the feeling.
6. Name the proof element that must sit directly below the hero to substantiate the claim.

Constraints:
- Do not invent metrics, customer names, or testimonials.
- Do not use the words leverage, seamless, innovative, cutting-edge, or game-changing.
- No em dashes.

Output format, in Markdown: **Claim audit** as a table with columns claim, verdict; then **Headline**, **Subhead**, **Primary CTA**, **Secondary CTA**, **Required proof**, each as a short labelled line, then three alternative headlines as a list.

## Tips

One claim, stated plainly, beats three claims stacked. If you cannot prove it on the page, do not write it.
