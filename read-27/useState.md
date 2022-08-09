# useState() Hook

## What was the motivation for introducing Hooks?

Hooks allow you to reuse stateful logic without changing your component hierarchy.

Hooks let you split one component into smaller functions based on what pieces are related (such as setting up a subscription or fetching data)

## What changes are important regarding implementing Hooks versus Component Classes?

Hooks let you use more of React’s features without classes.

## Hooks allow you to reuse stateful logic without changing **component**.

---

## Name two rules imposed by React Hook usage.

- **Only Call Hooks at the Top Level**
**Don’t call Hooks inside loops, conditions, or nested functions.** Instead, always use Hooks at the top level of your React function, before any early returns. By following this rule, you ensure that Hooks are called in the same order each time a component renders. That’s what allows React to correctly preserve the state of Hooks between multiple useState and useEffect calls.

- **Only Call Hooks from React Functions**
**Don’t call Hooks from regular JavaScript functions. Instead, you can:**

✅ Call Hooks from React function components.
✅ Call Hooks from custom Hooks

---

## What is a Hook?

Hooks are a new addition in React 16.8. They let you use state and other React features without writing a class.

## When would I use a Hook?

 If you write a function component and realize you need to add some state to it, previously you had to convert it to a class. Now you can use a Hook inside the existing function component. We’re going to do that right now!

 ```
 import React, { useState } from 'react';

function Example() {
  // Declare a new state variable, which we'll call "count"
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
```

```
class Example extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      count: 0
    };
  }

  render() {
    return (
      <div>
        <p>You clicked {this.state.count} times</p>
        <button onClick={() => this.setState({ count: this.state.count + 1 })}>
          Click me
        </button>
      </div>
    );
  }
}
```
