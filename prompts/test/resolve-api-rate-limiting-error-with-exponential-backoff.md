---
title: "Resolve API Rate Limiting Error with Exponential Backoff"
slug: resolve-api-rate-limiting-error-with-exponential-backoff
stage: Test
category: "Functional Bugs"
grade: A
score: 88
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/resolve-api-rate-limiting-error-with-exponential-backoff
---
# Resolve API Rate Limiting Error with Exponential Backoff

Implement a resilient retry mechanism with exponential backoff to handle 429 rate-limiting errors and improve API integration stability.

Variables: project_name, api_name, language, resourceId

## Prompt

You are a backend developer for {{project_name}}, which integrates with the {{api_name}} API. The application is making too many requests in a short period, causing the API to respond with a `429 Too Many Requests` error, which currently crashes the process. 

Your task is to implement a resilient retry mechanism with exponential backoff to handle API rate limiting gracefully.

**Context:**
- **Language:** {{language}} (e.g., Node.js, Python)
- **Library:** `axios` for Node.js or `requests` for Python.

**Current Fragile API Call:**

```javascript
// Node.js with axios
async function getResource(resourceId) {
  try {
    const response = await axios.get("https://api.{{api_name}}.com/v1/resources/{{resourceId}}");
    return response.data;
  } catch (error) {
    // This doesn't handle retries, just logs the error.
    console.error("API request failed:", error.response.status);
    throw error;
  }
}
```

**Instructions:**

1.  **Explain the Problem:** Describe what API rate limiting is and why simply failing on a `429` error is a poor strategy for a robust application.
2.  **Design a Retry Strategy:** Outline a strategy for retrying the API call. It must include:
    *   A maximum number of retries (e.g., 3 or 5).
    *   An exponential backoff algorithm to calculate the delay between retries (e.g., `delay = (2 ** attempt) * 1000` milliseconds).
    *   A check to only retry on a `429` status code and fail immediately on other errors like `404` or `500`.
3.  **Implement the Retry Logic:** Write a new function, `getResourceWithRetry

## Tips

A crucial backend skill, this prompt addresses how to build resilient integrations with external services.
