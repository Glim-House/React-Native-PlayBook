---
sidebar_position: 1
---

# React Native

[Official Documentation](https://reactnative.dev/)

React Native is a JavaScript framework that is used to develop mobile applications for iOS and Android.

## How React Native Works

A React Native app is made up of two sides, the JavaScript side and the native side. The native side could be Objective-C/Swift for iOS or Java/Kotlin for Android. The React Native Bridge allows the native code and the javascript code to talk to each other. Without the bridge, there is no way for the native code to send any information to the JavaScript code and vise versa.


There are two ways to build React Native apps such as **React Native CLI** and **Expo CLI**.

**Expo** is a framework that is used to build React Native apps. It is basically a bundle with tools and services built for React Native, that will help you get started with building React Native apps with ease.

## Why React Native CLI over Expo?

Why we prefer [React Native CLI](https://reactnative.dev/docs/environment-setup) beacuse its a built-in feature that helps you take control over the management of the project locally including the ability to choose our own dependencies, build tools, and configuration.

It provides the ability to create native modules, which allows to write code in native languages like Java or Objective-C, and then expose that code to the JavaScript layer.

We can use any third-party library or component, and can customize the app to our specific needs. Also we can integrate with other development tools such as version control systems like Git, continuous integration and delivery (CI/CD) systems, and various testing frameworks.You can not control the size of the app because the expo includes a pre-included library in SDK. (minimum prod build starts from 29MB-38MB).

## Debugging

**[Flipper](https://fbflipper.com/)** is Android & iOS Mobile debugging tools without using debug mode in react native.
Flipper has different plugins for debugging include `Layout`, `Network`, `Shared preferences`.

The greatest benefit of Flipper is not also many plugins but you can see Android / iOS device console debugging easily too.

The Flipper alert you about crash or network rejection too.












