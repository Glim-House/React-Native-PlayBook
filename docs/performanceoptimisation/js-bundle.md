---
sidebar_position: 1
---

# JS Bundle

## Enable Hermes

Hermes is a new JavaScript engine optimized for running React Native apps. its goal is to improve app performance.Using Hermes will result in improved start-up time, decreased memory usage, and smaller app size when compared to JavaScriptCore.

To enable Hermes make sure the project is running at least React Native version 0.64 or higher. Hermes is the default JavaScript engine in React Native 0.64 and above.

```yaml title='android/app/build.gradle'
project.ext.react = [
    enableHermes: true
]
```

After updating this you have to rebuild the project. Once your app finished building it should be running with Hermes as the JavaScript engine.

> Note that Hermes is not currently available for iOS, so this setup will only work for Android. If you want to use Hermes on iOS, you can use the --configuration hermes flag when building your app with Xcode.

[https://reactnative.dev/docs/hermes](https://reactnative.dev/docs/hermes)

## Tree shaking

Tree shaking is a technique that eliminates dead code from your bundle. It works by analyzing your code and identifying which functions and modules are actually used, and then removing the ones that aren't. This can significantly reduce the size of your bundle.
