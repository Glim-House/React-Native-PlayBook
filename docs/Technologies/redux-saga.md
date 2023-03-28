---
sidebar_position: 3
---

# Redux Saga

[Redux](https://redux-saga.js.org/) is used as a middleware to manage the whole app’s state in a centralised location called **store**. By using store all the components can reach the state, edit it and get the changes from other components.Sagas are implented by using [generator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Generator) functions.

## Rules
- Keep Sagas small and focused
- Use [yield effects](https://redux-saga.js.org/docs/Glossary) to handle side effects
- Use the appropriate [saga effect](https://redux-saga.js.org/docs/api/) for the task
- Use error handling: Working with asynchronous code, it's important to handle errors properly. Redux Saga provides a variety of ways to handle errors, such as try/catch blocks
- To dispatch an action, use the `put` effect.
- To access redux store, use `select` effect. 

## Structure and Naming

Inside `/redux` folder contains all the redux resources.
  - The `root reducer` file combines all the reducers.
  - The `root saga` file combines all the sagas into a single root saga.
  - The `configureStore` file contains the logic to configure the Redux store and middlewares.
  - For naming use **camel case**
    - saga name: `sagaName.saga.ts`
    - slice name: `sliceName.slice.ts`