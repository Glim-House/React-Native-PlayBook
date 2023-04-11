---
sidebar_position: 1
---

# App Bundle Optimisations

While working with react native apps, We all know that android builds are little bit heavier than comparing to other cross platform apps. We can reduce the app size with some simple steps.

## Enable proguard

Proguard is a tool that can slightly reduce the size of the APK. It does this by stripping parts of the React Native Java bytecode (and its dependencies) that your app is not using. Make sure to thoroughly test your app if you've enabled Proguard.

```yml title='android/app/build.gradle'
def enableProguardInReleaseBuilds = true
```

## Enable Separate Builds

If you’re looking for an alternative to the Android App bundle, this is the one to **Minimize App Size React Native** application. There are two major architectures supported by android devices: armeabi and x86. So when you generate the apk using React Native, react libraries are included in both architectures. So to generate two different are following command is used.

```yml title='android/app/build.gradle'
def enableSeparateBuildPerCPUArchitecture = true
```

## Webpack Bundle Analyzer

Webpack Bundle Analyzer is a tool used to visualize the packages your application is using. It won’t directly reduce the size of your bundle, but it can show you how much space each package takes up. Being able to see how much space each package occupies can better inform where you put your optimization efforts.

[https://www.npmjs.com/package/webpack-bundle-analyzer](https://www.npmjs.com/package/webpack-bundle-analyzer)
