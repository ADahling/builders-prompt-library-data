---
title: "Refactor a Class-based React Component to use Zustand for State Management"
slug: refactor-a-class-based-react-component-to-use-zustand-for-state-management
stage: Build
category: "Frontend & Styling"
grade: A
score: 83
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/refactor-a-class-based-react-component-to-use-zustand-for-state-management
---
# Refactor a Class-based React Component to use Zustand for State Management

Turn a class-based React counter into a functional component with a Zustand store, preserving increment, decrement, and reset actions.

## Prompt

We have a legacy codebase with several class-based React components that manage their own complex state using 'this.setState'. We are migrating our state management to Zustand for its simplicity and minimal boilerplate. 

Your task is to refactor a given class-based React component into a functional component that uses a Zustand store for its state management. The component is a simple counter that can increment, decrement, and reset its count.

The original class component looks like this:
```javascript
class Counter extends React.Component {
  constructor(props) {
    super(props);
    this.state = { count: 0 };
  }

  increment = () => this.setState({ count: this.state.count + 1 });
  decrement = () => this.setState({ count: this.state.count - 1 });
  reset = () => this.setState({ count: 0 });

  render() {
    return (
      <div>
        <h1>{this.state.count}</h1>
        <button onClick={this.increment}>Increment</button>
        <button onClick={this.decrement}>Decrement</button>
        <button onClick={this.reset}>Reset</button>
      </div>
    );
  }
}
```

Your refactored solution should:
1.  Create a Zustand store to manage the 'count' state and the 'increment', 'decrement', and 'reset' actions.
2.  Convert the 'Counter' class component into a functional component.
3.  Use the Zustand store within the new functional 'Counter' component to access the state and actions.
4.  The final component should have the exact same functionality and render the same UI as the original.

Provide the complete code for the Zustand store and the refactored functional component in a single TypeScript file.
