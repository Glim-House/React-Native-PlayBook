---
sidebar_position: 1
---

# UI

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
