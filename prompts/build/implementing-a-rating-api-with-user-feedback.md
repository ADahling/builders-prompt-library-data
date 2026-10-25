---
title: "Implementing a Rating API with User Feedback"
slug: implementing-a-rating-api-with-user-feedback
stage: Build
category: "API Design"
grade: C
score: 69
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/implementing-a-rating-api-with-user-feedback
---
# Implementing a Rating API with User Feedback

Design a rating API for item feedback with submission and retrieval endpoints, required fields, error handling, and duplicate prevention.

Variables: items, rating

## Prompt

Create a rating API for collecting user feedback on {{items}}. Discuss:
- Endpoints like {POST /ratings} to submit ratings and {GET /ratings/{itemId}} to fetch ratings for an item.
- Required fields for submissions, including {userId}, {itemId}, and {{rating}}.
- Response formats and error handling for invalid ratings.
- Strategies for preventing duplicate ratings from the same user.

## Tips

This prompt will help you manage user-generated feedback effectively.
