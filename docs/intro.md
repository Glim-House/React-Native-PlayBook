---
sidebar_position: 1
---

# React Native Playbook

React Native Playbook is a set of guidelines and best practices for setting up and developing React Native projects for enterprise applications. It provides a framework for building scalable and maintainable mobile applications with React Native.
The playbook includes a set of tools and techniques that can help developers create a robust development environment, optimize application performance, and improve code quality. It also includes recommendations for organizing code, managing dependencies, and implementing design patterns.
Some of the key features of the React Native Playbook include:

- Setup and configuration: The playbook provides a step-by-step guide for setting up the development environment, installing necessary dependencies, and configuring the project for production deployment.
- Code organization: The playbook suggests a modular approach to organizing code, separating components, screens, and utilities into separate directories to make the codebase more manageable.
- Design patterns: The playbook recommends implementing common design patterns like MVC, MVP, and MVVM to improve code maintainability and scalability.
- Testing and debugging: The playbook includes recommendations for implementing testing and debugging workflows to ensure the codebase is stable and bug-free.
- Performance optimization: The playbook provides guidance for optimizing application performance, including reducing bundle size, optimizing image loading, and implementing caching strategies.

By following the React Native Playbook, developers can streamline the development process, reduce the time and effort required to build enterprise applications, and ensure the codebase is scalable, maintainable, and high-performing.

## System Requirements

- Node JS
- Android Studio
- Xcode (Mac)

[Enviornment setup](https://reactnative.dev/docs/environment-setup)

## Create new Application

For create a new react native project, go to the terminal and run the command below.

```bash
npx react-native@latest init AwesomeProject
```

## Run application

To start metro server

```bash
npx react-native start
```

run android

```bash
npx react-native run-android
```

run ios

- open the `ios/project.xcodeworkspace` in xcode
- select a device type and click run button
