---
sidebar_position: 2
---

# React

[Official Documentation](https://react.dev/)

## PropTypes

- Documenting API used for type checking
```ts
const ReactComponent = (props) => {
  // ...implement render logic 
};
  
ReactComponent.propTypes = {
  propName1 : PropTypes.string,
  propName2 : PropTypes.bool,

  // ...prop type definitions
};
```

## Context

- Always use [context](https://react.dev/reference/react/createContext) when you have a clear need of it.
- Avoid putting all state data in a global context. If a state can stay local in a component, keep it local. Because every component that contains context data will update and re-render. 

## Refs
- Try to avoid using `refs`
  - Using refs to access DOM nodes or components can lead to tight coupling between your React components and the underlying implementation details, making it harder to refactor or maintain your code.
- Do not use string refs. All refs should use the callback style.