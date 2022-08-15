# useReducer

```
const [state, dispatch] = useReducer(reducer, initialArg, init);
```

## Why might the useReducer Hook be preferable to the useState Hook?

useReducer is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one. useReducer also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks.


## What are two ways to set the initial state?

There are two different ways to initialize useReducer state. You may choose either one depending on the use case. The simplest way is to pass the initial state as a second argument:
```
  const [state, dispatch] = useReducer(
    reducer,
    {count: initialCount}
  );
  ```


##



## What does useReducer return?

useReducer returns an array that holds the current state value and a dispatch


## The dispatch method

he dispatch function accepts an object that represents the type of action we want to execute when it is called. Basically, it sends the type of action to the reducer function to perform its job, which, of course, is updating the state.

The action to be executed is specified in our reducer function, which in turn, is passed to the useReducer. The reducer function will then return the updated state.


```
import { useReducer } from 'react';

// initial state of the database
const initialState = { count: 0 };

// API logic: how to update the database when the
// 'increment' API endpoint is called
const reducer = (state, action) => {
  if (action.type === 'increment') {
    return { count: state.count + action.payload };
  }
};

function App() {
  // you can think of this as initializing and setting
  // up a connection to the backend
  const [state, dispatch] = useReducer(reducer, initialState);

  return (
    <div>
      {/* Reading from the database */}
      Count: {state.count}
      {/* calling the API endpoint when the button is clicked */}
      <button onClick={() => dispatch({ type: 'increment', payload: 1 })}>
        +
      </button>
    </div>
  );
}

export default App;
```