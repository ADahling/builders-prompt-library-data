---
title: "Debounce Search-as-you-type Input to Prevent Excessive API Calls"
slug: debounce-search-as-you-type-input-to-prevent-excessive-api-calls
stage: Test
category: "Functional Bugs"
grade: A+
score: 98
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/debounce-search-as-you-type-input-to-prevent-excessive-api-calls
---
# Debounce Search-as-you-type Input to Prevent Excessive API Calls

Implement a debounce mechanism to optimize search-as-you-type functionality by reducing redundant API calls and preventing race conditions.

Variables: project_name, frontend_framework

## Prompt

You are a front-end developer building a "search-as-you-type" feature for {{project_name}}. The search input field triggers an API request on every single keystroke. This results in a massive number of unnecessary API calls, puts a heavy load on the backend, and can lead to race conditions where an earlier, slower request returns after a later, faster one, showing incorrect results.

Your task is to "debounce" the input to only trigger an API call after the user has stopped typing for a brief period.

**Context:**
- **Framework:** {{frontend_framework}}.
- **Problem:** Excessive API requests from an uncontrolled input.

**Buggy Keystroke Handler:**

```javascript
const SearchComponent = () => {
  const [query, setQuery] = useState(''');

  const handleChange = (e) => {
    const newQuery = e.target.value;
    setQuery(newQuery);
    // BUG: This runs on every single keystroke!
    fetchSearchResults(newQuery);
  };

  return <input type="text" value={query} onChange={handleChange} />;
};
```

**Instructions:**

1.  **Explain the Problem:** Describe the performance issues and potential race conditions caused by making an API request on every keystroke.
2.  **Implement a Debounce Hook/Function:** Create a custom React hook (`useDebounce`) or a generic debounce function. This function will take a value and a delay (e.g., 500ms) as input. It should only return the new value after the specified delay has passed without the value changing.
3.  **Refactor the Component:** Rewrite the `SearchComponent` to use your debouncing logic. The API call (`fetchSearchResults`) should now be triggered by the debounced value, not directly by the input's `onChange` event.

**Output Format:**

- **Problem Analysis:** A clear explanation of the issues with the current approach.
- **`useDebounce` Hook or Function:** The complete code for your reusable debouncing logic.
- **Refactored `SearchComponent`:** The corrected component that uses debouncing to control API requests.

## Tips

A classic and essential front-end performance optimization for any interactive search feature.
