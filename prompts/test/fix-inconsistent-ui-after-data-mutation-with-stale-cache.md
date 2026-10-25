---
title: "Fix Inconsistent UI After Data Mutation with Stale Cache"
slug: fix-inconsistent-ui-after-data-mutation-with-stale-cache
stage: Test
category: "Functional Bugs"
grade: A+
score: 96
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/fix-inconsistent-ui-after-data-mutation-with-stale-cache
---
# Fix Inconsistent UI After Data Mutation with Stale Cache

Resolve UI sync issues by implementing cache invalidation and optimistic updates after successful data mutations in modern fetch libraries.

Variables: library_name, tech_stack

## Prompt

You are a developer using a modern data-fetching library like {{library_name}} (e.g., React Query, SWR) in your {{tech_stack}} application. The application has a list of tasks. When a user marks a task as "complete" via a mutation, the API call succeeds, but the UI does not update to reflect the change. The task still appears as incomplete in the list until the page is manually refreshed.

This is because the mutation is not invalidating the cached data for the task list.

**Context:**
- **Library:** {{library_name}}
- **Queries:**
  - `useQuery(["tasks"], fetchTasks)` is used to fetch the list of all tasks.
- **Mutations:**
  - `useMutation(completeTask)` is used to update a task's status.

**Problematic Mutation Logic:**

```javascript
const TaskList = () => {
  const { data: tasks } = useQuery(["tasks"], fetchTasks);
  const completeTaskMutation = useMutation(completeTask, {
    // The onSuccess callback is missing the cache invalidation logic
    onSuccess: () => {
      console.log("Task completed successfully!");
    }
  });

  const handleComplete = (taskId) => {
    completeTaskMutation.mutate(taskId);
  };

  return (
    <ul>
      {tasks.map(task => (
        <li key={task.id}>
          {task.title} - {task.isComplete ? "Done" : "Pending"}
          <button onClick={() => handleComplete(task.id)}>Complete</button>
        </li>
      ))}
    </ul>
  );
};
```

**Instructions:**

1.  **Explain Stale Cache on Mutation:** Describe why the UI doesn't update automatically after the mutation succeeds. Explain the concept of a query cache in libraries like {{library_name}}.
2.  **Implement Cache Invalidation:** Using the tools provided by {{library_name}}, modify the `onSuccess` handler of the `useMutation` hook to invalidate the `["tasks"],` query. This will trigger an automatic re-fetch of the task list, ensuring the UI displays the correct, up-to-date information.
3.  **Discuss Optimistic Updates:** As an alternative, describe how you would implement an optimistic update for this scenario. Explain the process of immediately updating the UI with the expected new state and then rolling it back if the mutation fails.

**Output Format:**

- **Stale Cache Analysis:** An explanation of the caching problem.
- **Cache Invalidation Implementation:** The corrected `useMutation` hook with the `onSuccess` invalidation logic.
- **Optimistic Update Strategy:** A description and pseudo-code for implementing an optimistic update.

## Tips

A core concept when working with modern data-fetching libraries that manage server state.
