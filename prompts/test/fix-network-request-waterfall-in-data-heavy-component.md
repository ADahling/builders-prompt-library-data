---
title: "Fix Network Request Waterfall in Data-Heavy Component"
slug: fix-network-request-waterfall-in-data-heavy-component
stage: Test
category: "Functional Bugs"
grade: A+
score: 96
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-network-request-waterfall-in-data-heavy-component
---
# Fix Network Request Waterfall in Data-Heavy Component

Refactor sequential API calls into parallel requests using Promise.all to eliminate network waterfalls and decrease page load latency.

Variables: project_name, tech_stack, UserProfilePage.js, userId

## Prompt

You are a performance engineer tasked with optimizing a slow-loading user profile page in the {{project_name}} application. The page needs to display the user’s details, their recent posts, and their list of friends. The current implementation fetches this data in a sequence of three separate API calls, creating a "network request waterfall" where each request only begins after the previous one has completed. This significantly increases the total load time.

Your task is to refactor the data-fetching logic to run these requests in parallel.

**Context:**
- **Framework:** {{tech_stack}}
- **File:** ‘/path/to/{{UserProfilePage.js}}’

**Current Waterfall Implementation:**

```javascript
useEffect(() => {
  const fetchProfileData = async () => {
    // 1. Fetch user details
    const userRes = await axios.get("/api/users/{{userId}}");
    setUser(userRes.data);

    // 2. Fetch posts (waits for user details to finish)
    const postsRes = await axios.get("/api/users/{{userId}}/posts");
    setPosts(postsRes.data);

    // 3. Fetch friends (waits for posts to finish)
    const friendsRes = await axios.get("/api/users/{{userId}}/friends");
    setFriends(friendsRes.data);
  };

  fetchProfileData();
}, [userId]);
```

**Instructions:**

1.  **Analyze the Performance Issue:** Explain what a network request waterfall is and, using the provided code, illustrate how it leads to a longer total load time than necessary.
2.  **Refactor for Parallel Requests:** Rewrite the `fetchProfileData` function to initiate all three API requests concurrently. Use `Promise.all` to wait for all of them to complete before setting the state.
3.  **Handle Potential Errors:** Modify your parallel solution to correctly handle cases where one or more of the API calls might fail. The page should still attempt to render the data that was fetched successfully.

**Output Format:**

- **Waterfall Analysis:** A clear explanation of the performance bottleneck.
- **Parallel Data Fetching Code:** The refactored `fetchProfileData` function using `Promise.all`.
- **Error Handling Implementation:** The complete, robust function that includes error handling for the parallel requests.

## Tips

A common and high-impact performance optimization that every front-end developer should know.
