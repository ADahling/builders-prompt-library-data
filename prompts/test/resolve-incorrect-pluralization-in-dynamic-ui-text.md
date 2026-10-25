---
title: "Resolve Incorrect Pluralization in Dynamic UI Text"
slug: resolve-incorrect-pluralization-in-dynamic-ui-text
stage: Test
category: "Functional Bugs"
grade: A
score: 85
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/resolve-incorrect-pluralization-in-dynamic-ui-text
---
# Resolve Incorrect Pluralization in Dynamic UI Text

Implement locale-aware pluralization logic using the `Intl.PluralRules` API to ensure correct grammar across diverse languages in the UI.

Variables: project_name

## Prompt

You are a developer for {{project_name}}, a photo gallery application. The UI displays a message like "You have 1 photos" or "You have 2 photos". The plural "s" is simply added if the count is not 1. This works for English but fails for many other languages with more complex pluralization rules (e.g., Slavic languages have different forms for 1, 2-4, and 5+).

Your task is to fix this by using a proper, locale-aware pluralization solution.

**Context:**
- **Problem:** The pluralization logic is hardcoded for English rules.

**Instructions:**

1.  **Explain the Pluralization Challenge:** Describe why simple `count === 1 ? '' : 's'` logic is insufficient for a global application. Give an example of a language with different plural rules (e.g., Polish: 1 plik, 2 pliki, 5 plików).
2.  **Solution 1: Using `Intl.PluralRules`:** Write a function that uses the native `Intl.PluralRules` API. The function should take a count and a locale as input and return the correct plural category (e.g., `"one"

## Tips

Addresses a more advanced i18n topic that is often overlooked but is crucial for grammatical correctness.
