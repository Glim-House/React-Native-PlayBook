---
sidebar_position: 1
---

# React

[Official Documentation](https://react.dev/)

React is an open-source JavaScript library used for building user interfaces. It was developed by Facebook and released in 2013. React allows developers to create reusable UI components and compose them into complex UIs.

React is often used for building single-page applications and is particularly well-suited for building web applications with dynamic user interfaces. React utilizes a declarative programming model, where the developer specifies what the UI should look like, and React handles the updates and rendering of the UI based on changes to the application state.

## Features of React

- Declarative programming: React uses a declarative programming model, where the developer specifies what the UI should look like, and React handles the updates and rendering of the UI based on changes to the application state. This makes it easier to reason about the behavior of the UI, and to write code that is more concise and easier to maintain.

- Component-based architecture: React allows developers to create reusable UI components and compose them into complex UIs. This makes it easier to break down complex UIs into smaller, more manageable pieces, and to reuse those pieces across different parts of the application.

- Virtual DOM: React uses a virtual DOM, which is a lightweight representation of the actual DOM. This allows React to efficiently update the UI when changes occur, without having to manipulate the actual DOM directly. This approach can result in better performance, particularly for large and complex UIs.

- JSX: React uses JSX, which is a syntax extension that allows developers to write HTML-like code within JavaScript. This makes it easier to create and manipulate UI elements, and to combine HTML and JavaScript in a single file.

- Unidirectional data flow: React uses a unidirectional data flow, where data flows down from parent components to child components. This makes it easier to reason about the behavior of the UI, and to write code that is more predictable and easier to test.

- Developer tools: React has a rich set of developer tools, including the React Developer Tools browser extension, which allows developers to inspect and debug React applications.

## React components

React components are the building blocks of a React application. Components are essentially reusable pieces of UI that can be composed together to create a larger, more complex UI.

### Built-in components 

- `<Fragment>`, alternatively written as `<>...</>`, lets you group multiple JSX nodes together.
- `<Profiler>` lets you measure rendering performance of a React tree programmatically.
- `<Suspense>` lets you display a fallback while the child components are loading.
- `<StrictMode>` enables extra development-only checks that help you find bugs early.

```jsx
function ComponentName(props) {
  return <h1>Hello, {props.name}!</h1>;
}
```

## React Hooks

 Hooks are JavaScript functions that allow developers to use state and other React features in functional components. Hooks are functions that enable developers to add stateful logic to their functional components, which were previously only available in class components.

### Built-in hooks
#### useState
 useState allows functional components to manage state. It takes an initial value and returns an array with two elements - the current state value and a function to update the state value.

 ```jsx
 const [count, setCount] = useState(0);
```
#### useReducer
useReducer allows functional components to manage state through a reducer function. It takes a reducer function and an initial state value, and returns an array with two elements - the current state value and a dispatch function.

```jsx
const [state, dispatch] = useReducer(reducer, initialState);
```
#### useContext
Context lets a component receive information from distant parents without passing it as props.useContext allows functional components to consume a context that has been created by a React.createContext call. It takes the context object as its argument and returns its current value.

```jsx 
const value = useContext(SomeContext)
```

#### useRef 
useRef is a hook that allows to directly create a reference to the DOM element in the functional component. 
useRef returns a mutable ref object whose `.current` property is initialized to the passed argument. The ref object can be used to store any mutable value, updating a ref does not re-render your component.

```jsx
const ref = useRef(initialValue);
```

#### useEffect 
The useEffect hook is a smooth combination of React’s lifecycle methods like componentDidMount, componentDidUpdate and componentWillUnmount. 

- `callback` is a function that contains the side-effect logic. callback is executed right after the DOM update.
- `dependencies` is an optional array of dependencies. useEffect() executes callback only if the dependencies have changed between renderings.

```jsx
useEffect(callback,[dependencies]);
```

#### useMemo
useMemo hook returns a memoized value that helps in performance optimizations.It is a memoization technique that is used to avoid recomputing expensive values on every render cycle.

It takes two arguments: a function that returns the memoized value, and an array of dependencies that the function depends on. The function is only called when one of the dependencies changes, otherwise, it returns the cached value.

```jsx
const memoizedValue = useMemo(() => computeExpensiveValue(a, b), [a, b]);
```

#### useCallback
useCallback will return a memoized version of the callback that only changes if one of the dependencies has changed. This is useful when passing callbacks to optimized child components that rely on reference equality to prevent unnecessary renders

```jsx
const memoizedCallback = useCallback(() => {
    doSomething(a, b);
  },[a, b]);
```