---
sidebar_position: 1
---

# UI Optimisations

From the codebase, a react native app needs a lot of optimisation for UI side, for solve the issues like frame droops, UI failures etc.

## Optimising large lists

For apps with large list, It challenging to keep the frame rates smooth especially while scrolling, and sometimes its likely to run out of memory. For solve those issues we can use `Flashlist` instead of `Flatlist`

A drop-in replacement of Flatlist, with 5x improvement on UI thread and 10x on JS thread. It does better memory management by avoiding recreation of items as users scroll through the list. It also offers features like sticky headers, pull to refresh, etc.

[https://shopify.github.io/flash-list/](https://shopify.github.io/flash-list/)

## Memoize React Components

Memoization optimizes the performance of a function by storing the results of expensive function calls and returning the stored results when the same inputs occur again. It helps you avoid recalculating the results each time the function is called.

```js
import React from "react";
function TestComponent(props) {
  return <Text>{props.text}</Text>;
}
export default React.memo(TestComponent);
```

## Responsiveness issues

- **Avoid Hardcoded Values** - An app may become unresponsive when sizes, margins, and locations are hardcoded. Create a responsive user interface instead by using relative scaling, platform-specific design, and media queries.
- **Utilize Flexbox** - A responsive user interface can be made using the potent layout technology known as Flexbox. It offers a versatile method of organising elements on the screen without requiring manual adjustment of margins, sizes, and placements.

```js
import React, { Component } from "react";
import { View, Text } from "react-native";

export default class MyLayout extends Component {
  render() {
    const flexD = "column";
    return (
      <View style={{ flex: 1, flexDirection: flexD, backgroundColor: "#fff" }}>
        <View style={{ flex: 1, backgroundColor: "#808080" }}>
          <Text>'Head'</Text>
        </View>
        <View style={{ flex: 6, backgroundColor: "#D3D3D3" }}>
          <Text>'Body'</Text>
        </View>
        <View style={{ flex: 1, backgroundColor: "#808080" }}>
          <Text>'Foot'</Text>
        </View>
      </View>
    );
  }
}
```

- **Use Platform-specific Styling** - Platform-specific code can be written using React Native and then converted into native code for each platform. Developers can use this to build platform-specific styles for their components, ensuring that they appear and function as intended across all platforms.

```js
<Button
  title="Click Here"
  style={Platform.OS === "ios" ? styles.iosButton : styles.androidButton}
>
  Click Here
</Button>
```
