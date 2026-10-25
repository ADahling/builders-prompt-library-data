---
title: "Implement a Redux Toolkit Store with an Async Thunk for API Data Fetching"
slug: implement-a-redux-toolkit-store-with-an-async-thunk-for-api-data-fetching
stage: Build
category: "Frontend & Styling"
grade: B
score: 78
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/implement-a-redux-toolkit-store-with-an-async-thunk-for-api-data-fetching
---
# Implement a Redux Toolkit Store with an Async Thunk for API Data Fetching

Get a single TypeScript file with a Redux Toolkit user slice, async thunk, store, and React component for API fetching with loading and error states.

## Prompt

Our React application uses Redux for state management, and we are migrating to Redux Toolkit for simplification. We need to fetch a list of users from an API and store them in the Redux store.

Your task is to set up a Redux Toolkit slice for managing users and create an async thunk to handle the API request.

The implementation must:
1.  Use 'createSlice' from Redux Toolkit to define the user slice, including its name, initial state, and reducers.
2.  The slice should handle three states for the data fetching process: 'loading', 'succeeded', and 'failed'.
3.  Use 'createAsyncThunk' to create an action that performs the asynchronous API call to fetch users from a placeholder API (e.g., JSONPlaceholder).
4.  The slice's reducers should be updated based on the promise lifecycle of the async thunk (pending, fulfilled, rejected).
5.  Configure a Redux Toolkit store using 'configureStore' and include the user slice in it.
6.  Provide a simple React component that dispatches the async thunk and displays the list of users or a loading/error message.

Provide the complete code in a single TypeScript file, including the user slice, the store configuration, and the React component that uses it.
