# Component Based UI

React is a component based web development library for making user interfaces

## What are the building blocks of a React app?

- elements and components.

## What is the difference between an element and a React component?

***Elements*** are the smallest building blocks of React apps.

An element describes what you want to see on the screen:
```
const element = <h1>Hello, world</h1>;
```
Unlike browser DOM elements, React elements are plain objects, and are cheap to create. React DOM takes care of updating the DOM to match the React elements.

***components*** are like JavaScript functions. They accept arbitrary inputs (called “props”) and return React elements describing what should appear on the screen.

## What are some advantages of React’s component based architecture?

- Reusability: In Component Driven Development, the development process is in place, components once created can be easily used across as many modules as needed. Reusability helps to provide the development efforts and cost across applications.

---
## introducing JSX

## What is JSX and why do we use it?

JSX stands for JavaScript XML.

JSX allows us to write HTML elements in JavaScript and place them in the DOM without any createElement()  and/or appendChild() methods.

JSX converts HTML tags into react elements.


## Describe the process of embedding JavaScript expressions in JSX.

Embedding Expressions in JSX
In the example below, we declare a variable called name and then use it inside JSX by wrapping it in curly braces:
```
const name = 'Josh Perez';
const element = <h1>Hello, {name}</h1>;
```
You can put any valid JavaScript expression inside the curly braces in JSX. For example, 2 + 2, user.firstName, or formatName(user) are all valid JavaScript expressions.

---

## rendering elements

## Explain what a React Component

React Components
Components are independent and reusable bits of code. They serve the same purpose as JavaScript functions, but work in isolation and return HTML.

Components come in two types, Class components and Function components, in this tutorial we will concentrate on Function components.

## Describe mutability and React Components, specifically, how is the UI updated?



React elements are immutable. Once you create an element, you can’t change its children or attributes. An element is like a single frame in a movie: it represents the UI at a certain point in time.

With our knowledge so far, the only way to update the UI is to create a new element, and pass it to root.render().

Consider this ticking clock example:
```
const root = ReactDOM.createRoot(
  document.getElementById('root')
);

function tick() {
  const element = (
    <div>
      <h1>Hello, world!</h1>
      <h2>It is {new Date().toLocaleTimeString()}.</h2>
    </div>
  );
  root.render(element);
}

setInterval(tick, 1000);
```

## f changes are made to the UI, what does React update?

React DOM compares the element and its children to the previous one, and only applies the DOM updates necessary to bring the DOM to the desired state.

 