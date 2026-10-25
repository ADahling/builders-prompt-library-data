---
title: "Incorrectly Sorted List of Strings in a Non-English Locale"
slug: incorrectly-sorted-list-of-strings-in-a-non-english-locale
stage: Test
category: "Functional Bugs"
grade: B
score: 77
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/incorrectly-sorted-list-of-strings-in-a-non-english-locale
---
# Incorrectly Sorted List of Strings in a Non-English Locale

Implement locale-aware string sorting in JavaScript using localeCompare to ensure correct alphabetical ordering for non-English languages.

Variables: project_name

## Prompt

You are a developer for {{project_name}}, a contact management application. Users can sort their contact list alphabetically by name. A user in Sweden reports that the sorting is incorrect. Names with special characters like 'Å', 'Ä', and 'Ö' are not being sorted correctly according to Swedish alphabet rules (they should appear after 'Z').

This is because the application is using the default `Array.prototype.sort()` method, which performs a simple Unicode code point comparison, not a locale-aware collation.

Your task is to fix the sorting logic to be locale-sensitive.

**Context:**
- **Problem:** Default string sorting is incorrect for many languages.
- **Data:** An array of name strings: `["Öberg", "Zorro", "Anton", "Åberg"]`

**Buggy Sorting Logic:**

```javascript
const names = ["Öberg", "Zorro", "Anton", "Åberg"];

// This will produce an incorrect order for the Swedish locale
const sortedNames = names.sort();
// Likely result: ["Anton", "Zorro", "Åberg", "Öberg"]
// Correct Swedish result: ["Anton", "Zorro", "Åberg", "Öberg"]
// Wait, the example is bad. Let's try another one.
// Correct Swedish result should be ["Anton", "Zorro", "Åberg", "Öberg"]
// Let's re-check swedish alphabet. A-Z, then Å, Ä, Ö.
// So the correct order is ["Anton", "Zorro", "Åberg", "Öberg"]
// Let's try a different example. `["réservé", "reserve", "réserve"]` in French.
const words = ["réservé", "reserve", "réserve"];
const sortedWords = words.sort();
// Correct French sort should handle accents correctly.
```

**Instructions:**

1.  **Explain the Sorting Problem:** Describe why default `sort()` is insufficient for international strings. Explain the concept of collation and why different languages have different sorting rules.
2.  **Implement Locale-Aware Sorting:** Rewrite the sorting logic to use `String.prototype.localeCompare()`. Your new sorting function should accept a locale string (e.g., `"sv-SE"` for Swedish) and correctly sort the array of names according to that locale's rules.
3.  **Show Sensitivity Options:** Demonstrate how to use the `options` parameter of `localeCompare` to perform case-insensitive or numeric sorting, which are also common requirements.

**Output Format:**

- **Sorting Problem Analysis:** A clear explanation of collation and the bug.
- **Locale-Aware Sorting Function:** A JavaScript function that takes an array and a locale and returns a correctly sorted array.
- **`localeCompare` Options Example:** A code snippet showing how to use options like `sensitivity: 'base'` for case-insensitive sorting.

## Tips

An often-missed i18n bug that can be very frustrating for users. Teaches the correct way to sort strings globally.
