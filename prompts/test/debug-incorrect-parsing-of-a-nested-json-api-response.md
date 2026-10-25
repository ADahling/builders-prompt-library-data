---
title: "Debug Incorrect Parsing of a Nested JSON API Response"
slug: debug-incorrect-parsing-of-a-nested-json-api-response
stage: Test
category: "Functional Bugs"
grade: A+
score: 97
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/debug-incorrect-parsing-of-a-nested-json-api-response
---
# Debug Incorrect Parsing of a Nested JSON API Response

Refactor fragile JSON parsing logic using optional chaining and nullish coalescing to prevent application crashes from missing API data.

Variables: project_name

## Prompt

You are a developer on the {{project_name}} team, working with a third-party API that provides user data. The API returns a complex, nested JSON object. A bug is causing the application to crash because the code is attempting to access a property on an object that is sometimes missing from the API response.

Your task is to debug the data parsing logic and make it resilient to variations in the JSON structure using optional chaining and nullish coalescing.

**Context:**
- **API Response Structure (Ideal Case):**
  ```json
  {
    "id": 123,
    "personalInfo": {
      "name": "John Doe",
      "address": {
        "city": "New York"
      }
    },
    "company": {
      "name": "Tech Corp"
    }
  }
  ```
- **API Response Structure (Problem Case):** Sometimes, the `address` or `company` object is missing.
  ```json
  {
    "id": 456,
    "personalInfo": {
      "name": "Jane Smith"
    }
  }
  ```

**Buggy Data Access Code:**

```javascript
const displayUserData = (user) => {
  // This line will crash if user.personalInfo.address is undefined
  const city = user.personalInfo.address.city;
  const companyName = user.company.name;

  console.log('City:', city);
  console.log('Company:', companyName);
};
```

**Instructions:**

1.  **Identify the Crashing Code:** Pinpoint the exact lines that will throw a `TypeError` and explain why.
2.  **Rewrite with Optional Chaining:** Refactor the `displayUserData` function to use the optional chaining operator (`?.`) to safely access nested properties that may not exist.
3.  **Use Nullish Coalescing for Defaults:** Further improve the code by using the nullish coalescing operator (`??`) to provide default values (e.g., ‘N/A’) for the `city` and `companyName` variables when they are not found in the API response.
4.  **Explain the Benefits:** Describe why this modern JavaScript approach is superior to traditional methods like nested `if` checks or using the `&&` operator for checking property existence.

**Output Format:**

- **Crash Analysis:** A clear explanation of the `TypeError` bug.
- **Robust Data Access Code:** The corrected `displayUserData` function using `?.` and `??`.
- **Explanation of the Benefits:** A summary of why the new approach is better.

## Tips

A very practical prompt that teaches modern, safe, and clean ways to handle complex API responses.
