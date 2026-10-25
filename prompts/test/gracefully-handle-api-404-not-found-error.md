---
title: "Gracefully Handle API 404 Not Found Error"
slug: gracefully-handle-api-404-not-found-error
stage: Test
category: "Functional Bugs"
grade: A+
score: 98
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/gracefully-handle-api-404-not-found-error
---
# Gracefully Handle API 404 Not Found Error

Implement error handling and conditional rendering in a data-fetching component to prevent crashes and display user-friendly 404 messages.

Variables: project_name, tech_stack, PostPage.js, postId

## Prompt

You are a front-end developer working on a {{project_name}} blog platform using {{tech_stack}}. The application has a page that displays a single blog post, fetched by its ID. A bug has been reported: when a user tries to access a post that does not exist (e.g., via a mistyped URL), the application crashes or shows a generic, unhelpful error page.

Your task is to improve the data-fetching logic to gracefully handle a 404 (Not Found) error from the API and display a user-friendly message.

**Context:**
- **Framework:** {{tech_stack}}
- **Data Fetching:** Using the `fetch` API or `axios`.
- **File:** '/path/to/{{PostPage.js}}'

**Current Data Fetching Logic:**

```javascript
const PostPage = ({ postId }) => {
  const [post, setPost] = useState(null);

  useEffect(() => {
    const fetchPost = async () => {
      // This call will fail with a 404 if the post doesn't exist
      const response = await axios.get("/api/posts/{{postId}}");
      // The code doesn't handle the error case, leading to a crash when trying to access response.data
      setPost(response.data);
    };

    fetchPost();
  }, [postId]);

  // This will crash if post is null
  return (
    <div>
      <h1>{post.title}</h1>
      <p>{post.content}</p>
    </div>
  );
};
```

**Instructions:**

1.  **Identify the Missing Error Handling:** Explain why the current code fails when the API returns a 404 status code.
2.  **Implement `try...catch`:** Rewrite the `fetchPost` function to include a `try...catch` block to handle potential errors during the API call.
3.  **Check for 404 Status:** Inside the `catch` block, specifically check if the error was due to a 404 status. If so, set a state variable to indicate that the post was not found.
4.  **Render a User-Friendly Not Found Message:** Modify the component’s return statement to display a helpful message like "Sorry, the post you are looking for does not exist." when the post is not found. It should also continue to show a loading state while the request is in progress.

**Output Format:**

- **Error Handling Analysis:** A clear explanation of the bug.
- **Corrected Component Code:** The complete, fixed `PostPage` component with proper loading and not-found states.
- **Explanation of the Fix:** A summary of how the new logic gracefully handles the 404 error.

## Tips

A fundamental prompt for teaching basic error handling in asynchronous data fetching.
