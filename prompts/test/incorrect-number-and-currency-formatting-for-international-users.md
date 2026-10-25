---
title: "Incorrect Number and Currency Formatting for International Users"
slug: incorrect-number-and-currency-formatting-for-international-users
stage: Test
category: "Functional Bugs"
grade: B
score: 77
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/incorrect-number-and-currency-formatting-for-international-users
---
# Incorrect Number and Currency Formatting for International Users

Implement locale-aware number and currency formatting using the JavaScript Intl API to fix region-specific display bugs in e-commerce apps.

Variables: project_name

## Prompt

You are a developer for {{project_name}}, an e-commerce platform. A user from Germany has reported that product prices and review counts are displayed in an incorrect format. For example, a price of "1,299.99" (USD) is being shown, but in Germany, this should be formatted as "1.299,99". Similarly, a count of "10000" should be "10.000".

This is because the application is using basic string formatting or `Number.prototype.toString()` instead of a locale-aware formatting API.

Your task is to fix this using the built-in `Intl` API.

**Context:**
- **Problem:** Numbers and currencies are not formatted according to the user's locale.

**Instructions:**

1.  **Explain the Formatting Issue:** Describe why number and currency formats vary across locales and why relying on default string conversion is a bug.
2.  **Implement Locale-Aware Number Formatting:** Write a function that takes a number and a locale string (e.g., `"de-DE"

## Tips

Teaches the use of the powerful and native `Intl` API for a very common i18n requirement.
