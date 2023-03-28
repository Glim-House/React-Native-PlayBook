---
sidebar_position: 1
---

# Env

For use enviornment variables in react native project, the most recommended way is to use a package named `react-native-dotenv`. This babel plugin lets you inject your environment variables into your Javascript environment using dotenv for multiple environments.

[Official Documentation](https://www.npmjs.com/package/react-native-dotenv)

## Installation

```bash
npm install react-native-dotenv
```

include the package into `.babelrc` file. If the file does not exist, just create it.

```json
{
  "plugins": [["module:react-native-dotenv"]]
}
```

Create a new .env file in the root of your project project directory

```
API_URL=https://api.example.org
API_TOKEN=abc123
```

After all this restart your project and check all working fine.

## Usage

You can use the environment variables in the files like this:

```js
import { API_URL, API_TOKEN } from "@env";

fetch(`${API_URL}/users`, {
  headers: {
    Authorization: `Bearer ${API_TOKEN}`,
  },
});
```
