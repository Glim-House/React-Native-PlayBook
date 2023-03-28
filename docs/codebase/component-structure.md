---
sidebar_position: 4
---

# Component Structure

## Sample component

```ts
import { View, Text } from "react-native";
import React from "react";

interface Props {
  /**
   * Description of the prop
   */
  name: string;
}

/**
 * @name Dummy Component
 * @description lorem ipsum dolor sit amet, consectetur adipiscing
 * @author Authorname
 * @returns
 */
const DummyComponent = ({ name }: Props) => {
  try {
    return (
      <View>
        <Text>{name}</Text>
      </View>
    );
  } catch (error) {
    // Actions that done when error is thrown
  }
};

export default DummyComponent;
```

## A Component must have

- proper comments
- component level exception handling
- proper import statements
