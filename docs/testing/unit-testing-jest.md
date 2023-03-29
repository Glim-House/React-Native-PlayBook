---
sidebar_position: 2
---

# Unit Testing

A unit test is a piece of code that tests the behavior of a function or class, usually written by developers.

## Testing frameworks

- Jest [https://jestjs.io/](https://jestjs.io/)
- Mocha [https://mochajs.org/](https://mochajs.org/)
- Selenium [https://www.selenium.dev/](https://www.selenium.dev/)

Most recommented testing framework for react native application is to use **Jest** framework.

## Snapshot testing

Snapshot test is the most commonly accepted testing method for react native component to ensure the code block functionality. Once we initiate the test, it will create a snapshot of the component in the respective folder and it will compare the component with snpashot on every changes.

First we need to create a test file

```js title="__tests__/Intro-test.js"
import React from "react";
import renderer from "react-test-renderer";
import Intro from "../Intro";

test("renders correctly", () => {
  const tree = renderer.create(<Intro />).toJSON();
  expect(tree).toMatchSnapshot();
});
```

When you run `yarn test` or `jest`, this will produce an output file.

> The snapshot should be commited to git along with component

## standards

- always keep test files inside the component folder
- test file name should be prefixed with **test**. eg: `component.test.js`

## References

- [https://jestjs.io/docs/tutorial-react-native](https://jestjs.io/docs/tutorial-react-native)
