---
sidebar_position: 3
---

# Linting

Linting is a process that allows us to maintain code quality and enforce code conventions.

- ESLint is the compound language of ES(EcmaScript) + Lint(show error code), and analyzes the source code, and the tool that helps to make them the same style.
- Prettier is a Code Formatter, makes the same code style by rules.
- Husky is an NPM package which utilizes GIT hooks to integrate tools and increase quality code submissions to your repository.

## Commonly used method

Customise the prettierrc as below:

```js title=".prettierrc.js"
module.exports = {
  arrowParens: "avoid",
  bracketSameLine: true,
  bracketSpacing: false,
  singleQuote: true,
  trailingComma: "all",
};
```

For eslint we are extending the community package

```js title=".eslintrc.js"
module.exports = {
  root: true,
  extends: "@react-native-community",
};
```

## References

- [Getting Started with ESLint](https://eslint.org/docs/latest/use/getting-started)
