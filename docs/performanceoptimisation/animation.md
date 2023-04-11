---
sidebar_position: 1
---

# Animation

## runOnUI and runOnJS

When we are working with animation, we are not sure that its working on UI thread or JS thread. For making this more transparent, Reanimated indroduces `runOnUI` and `runOnJS`.

runOnUI enables executing worklet functions on the UI thread. Note that UI execution is asynchronous from the caller’s perspective. When you pass arguments, they will be copied to the UI context.

```js
const onPress = () => {
  runOnUI(someWorklet)("Howdy");
};
```

runOnJS which calls a callback asynchronously. An exception will be thrown if you call a JS callback without this function.

```js
useDerivedValue(() => {
  runOnJS(externalLibraryFunction)(args);
});
```
