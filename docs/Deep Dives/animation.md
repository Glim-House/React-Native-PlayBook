---
sidebar_position: 1
---

# Animations

Animation is the process of adding a motion effect to a view, image, or a text to increate user experience. In react native, there are many animation libraries are available like:

- Re-Animated [https://docs.swmansion.com/react-native-reanimated/](https://docs.swmansion.com/react-native-reanimated/)
- Moti [https://moti.fyi/](https://moti.fyi/)

We highly recommend to use React Native reanimated to enterprise projects. Because, it have higher performance and better communiy support.

## Use of shared values

Simply says shared values are the animation controlling variables inside a component. for every animation declare a new shared value:

```js
const sharedVal = useSharedValue(3.1415);
```

There is a hook available named `useDerivedValue` to creating shared value reference that can change in response to updating of one or more other shared values.

```js
const App = () => {
  const [state, setState] = useState(0);
  const sv = useSharedValue(state);

  const derived = useDerivedValue(() => {
    return sv.value * state;
  }, dependencies);
  //...
  return <></>;
};
```

> Don't use shared values to conditional rendering or other logical functions. It may lead to app crashes.

## Use of worklets

Basically worklets are the small js blocks that works along with animations.

```js
function someWorklet(greeting) {
  "worklet";
  console.log(greeting, "From the UI thread");
}

function onPress() {
  runOnUI(someWorklet)("Howdy");
}
```

use of **worklets**, **runOnUi**, **runOnJs**, etc will help the animation to work smoothly without any framedrops.

## Shared Element Transition

Currently shared element transitions by reanimated is under experiaments. [https://docs.swmansion.com/react-native-reanimated/docs/api/sharedElementTransitions](https://docs.swmansion.com/react-native-reanimated/docs/api/sharedElementTransitions)

So, meantime we can use `react-native-shared-element` [https://github.com/IjzerenHein/react-native-shared-element](https://github.com/IjzerenHein/react-native-shared-element)

## Some References

- [https://docs.swmansion.com/react-native-reanimated/docs/api/LayoutAnimations/customAnimations](https://docs.swmansion.com/react-native-reanimated/docs/api/LayoutAnimations/customAnimations)
- [https://docs.swmansion.com/react-native-reanimated/docs/api/miscellaneous/interpolate](https://docs.swmansion.com/react-native-reanimated/docs/api/miscellaneous/interpolate)
- [https://docs.swmansion.com/react-native-reanimated/docs/fundamentals/layout_animations](https://docs.swmansion.com/react-native-reanimated/docs/fundamentals/layout_animations)
