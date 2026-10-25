---
title: "Build a Draggable Kanban Board with React and a Drag-and-Drop Library"
slug: build-a-draggable-kanban-board-with-react-and-a-drag-and-drop-library
stage: Build
category: "Frontend & Styling"
grade: A+
score: 93
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/build-a-draggable-kanban-board-with-react-and-a-drag-and-drop-library
---
# Build a Draggable Kanban Board with React and a Drag-and-Drop Library

Get a React TypeScript Kanban component for a project management tool, with draggable tasks, cross-column moves, state updates, and visual feedback.

Variables: tool_name

## Prompt

We are developing a project management tool, {{tool_name}}, and a core feature is a Kanban board where users can drag and drop tasks between columns (e.g., 'To Do', 'In Progress', 'Done').

Create a React component for a Kanban board using a popular drag-and-drop library like 'react-beautiful-dnd' or '@dnd-kit/core'.

The Kanban board should:
1.  Display multiple columns, each with a title and a list of tasks.
2.  Allow users to drag tasks within the same column to reorder them.
3.  Allow users to drag tasks from one column to another.
4.  The state of the board (the columns and the tasks within them) should be managed in the React component's state.
5.  When a drag operation is completed, the component's state should be updated to reflect the new position of the task.
6.  The implementation should be visually clean and provide clear feedback to the user during the drag operation (e.g., changing background color of the drop zone).

Provide the complete code for the Kanban board component in a single TypeScript file. Include the initial state structure and the logic for handling the 'onDragEnd' event to update the state. You can choose either 'react-beautiful-dnd' or '@dnd-kit/core' for the implementation.
