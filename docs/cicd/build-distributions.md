---
sidebar_position: 1
---

# Build Distributions

IN the development phase, we have to distribute the development build to the testers periodically for testing purposes. So, we use **Diawi** fro the same.
Diawi is a tool for developers to deploy development apps directly to the devices. It will work on ios and android devices.

## Android

In android you can take the development build with the following command:

```bash
cd android && ./gradlew assembleRelease
```

It will create an .apk build in `android/app/build/outputs/apk/release/app-release.apk`. You can directly upload the build into diawi.

## iOS

For ios, first we have to archive the build, and select **adhoc** in the upload method. It will build and .ipa file in respective directory. You can directly upload the ipa build into diawi.

## References

- [https://www.diawi.com/](https://www.diawi.com/)
