---
sidebar_position: 1
---

# Animation Optimisations

From a developer perspective react native animations needs a lots of optimisation. Otherwise it leads to app crashes and poor user experience. There are some common performance issues faced by animations:

- Overloading the main thread
- Frame drop in devices with more than 60 FPS
- App crashes

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

## Layout Animations

In React Native every component appears instantly whenever you add it to the component hierarchy. It's not something we are used to in the real world. Layout Animations are here to address the problem and help you animate an appearance of any view.
There are many predefined animations grouped by thier type to implement the aimations easily, such as fadein, bouncein, slideup etc.

```js
<AnimatedComponent entering={AnimationName.duration(3000).otherModifier()} >
```
