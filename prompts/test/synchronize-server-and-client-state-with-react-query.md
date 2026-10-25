---
title: "Synchronize Server and Client State with React Query"
slug: synchronize-server-and-client-state-with-react-query
stage: Test
category: "Functional Bugs"
grade: B
score: 79
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/synchronize-server-and-client-state-with-react-query
---
# Synchronize Server and Client State with React Query

Refactor manual React data fetching to TanStack Query to automate caching, background synchronization, and efficient server state management.

Variables: project_name, app_type, tech_stack

## Prompt

You are a senior front-end engineer working on {{project_name}}, a highly interactive {{app_type}} built with {{tech_stack}}. The application heavily relies on data fetched from a server, but it suffers from stale data issues. For example, if a user updates a project's name on one page, the old name is still shown in the project list on another page until the browser is manually refreshed.

Your task is to replace the existing `useEffect`/`useState` data fetching logic with `React Query` (or a similar library like SWR) to provide a robust, auto-managed, and synchronized state management solution for server state.

**Context:**
- **Problem:** Manual server state management is complex and error-prone.
- **Goal:** Implement a modern data-fetching library to handle caching, re-fetching, and state synchronization automatically.

**Existing Manual Fetching Logic:**

```javascript
const ProjectList = () => {
  const [projects, setProjects] = useState([]);
  const [isLoading, setIsLoading] = useState(true);

  useEffect(() => {
    setIsLoading(true);
    axios.get('/api/projects')
      .then(res => setProjects(res.data))
      .finally(() => setIsLoading(false));
  }, []); // Empty dependency array means this only runs once

  if (isLoading) return <div>Loading...</div>;
  return <ul>{projects.map(p => <li key={p.id}>{p.name}</li>)}</ul>;
};
```

**Instructions:**

1.  **Analyze the Flaws of Manual Fetching:** Describe the problems with the current `useEffect`-based approach, focusing on stale data, lack of re-fetching on window focus, and the boilerplate code required.
2.  **Refactor to `React Query`:** Rewrite the `ProjectList` component using the `useQuery` hook from `React Query`. Also, show how to set up the `QueryClientProvider` at the root of the application.
3.  **Implement Mutation and Cache Invalidation:** Create a separate component, `UpdateProjectNameForm

## Tips

A very practical prompt that guides developers toward modern best practices for managing server state.
