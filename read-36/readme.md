#  State with Redux


![](../image/exercises/ReduxDataFlow.gif)



## **What is Redux?**

Redux is a pattern and library for managing and updating application state, using events called "actions". It serves as a centralized store for state that needs to be used across your entire application, with rules ensuring that the state can only be updated in a predictable fashion.

## **Why Should I Use Redux?**
Redux helps you manage "global" state - state that is needed across many parts of your application.

The patterns and tools provided by Redux make it easier to understand when, where, why, and how the state in your application is being updated, and how your application logic will behave when those changes occur. Redux guides you towards writing code that is predictable and testable, which helps give you confidence that your application will work as expected.

## **When Should I Use Redux?**
Redux helps you deal with shared state management, but like any tool, it has tradeoffs. There are more concepts to learn, and more code to write. It also adds some indirection to your code, and asks you to follow certain restrictions. It's a trade-off between short term and long term productivity.

# **The Redux Store**
The center of every Redux application is the store. A "store" is a container that holds your application's global state.

A store is a JavaScript object with a few special functions and abilities that make it different than a plain global object:

You must never directly modify or change the state that is kept inside the Redux store
Instead, the only way to cause an update to the state is to create a plain action object that describes "something that happened in the application", and then dispatch the action to the store to tell it what happened.
When an action is dispatched, the store runs the root reducer function, and lets it calculate the new state based on the old state and the action
Finally, the store notifies subscribers that the state has been updated so the UI can be updated with the new data..


# Redux Terminology

**Actions**
An action is a plain JavaScript object that has a type field. You can think of an action as an event that describes something that happened in the application.

**Reducers**
A reducer is a function that receives the current state and an action object, decides how to update the state if necessary, and returns the new state: (state, action) => newState. You can think of a reducer as an event listener which handles events based on the received action (event) type.

**Store**
The current Redux application state lives in an object called the store .

**Dispatch**
The Redux store has a method called dispatch. The only way to update the state is to call store.dispatch()

**Selectors**
Selectors are functions that know how to extract specific pieces of information from a store state value. As an application grows bigger, this can help avoid repeating logic as different parts of the app need to read the same data:


## Core Concepts and Principles

- **Single Source of Truth**
The global state of your application is stored 

- **State is Read-Only**
The only way to change the state is to dispatch an action, an object that describes what happened.

- **Changes are Made with Pure Reducer Functions**
To specify how the state tree is updated based on actions, you write reducer functions. Reducers are pure functions that take the previous state and an action, and return the next state. Like any other functions, you can split reducers into smaller functions to help do the work, or write reusable reducers for common tasks.
