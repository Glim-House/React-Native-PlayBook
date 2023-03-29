---
sidebar_position: 2
---

# Standards

## Development Release

### Android

- Change the environment to qa (or respective env)
- Clean build folder `cd android && ./gradlew clean`
- Create Build `cd android && ./gradlew assembleRelease`
- This will create an APK file and distribute the APK for testing.

### Ios

- Change the environment to qa (or respective env)
- Open Xcode, change version, build number and the device target to any ios Device
- In the top menu choose product → clean build folder
- In the top menu select product → archive (This process will take some time)
- After completing the Archive process, A dialogue will appear, select the release method and click the “Distribute App” button.
- Then choose `App Store Connect` and click on Next.
- After completing the process, the app will be uploaded in test flight and available for testing.
- Go to app store connect [https://play.google.com/console/u/0/developers](https://appstoreconnect.apple.com/login) to see the builds

## Production Release

### Android

- Change the environment to prod
- Change version and build number
- Clean build folder `cd android && ./gradlew clean`
- Open the android folder in Android Studio
- In the top menu choose to Build → Generate signed APK or Bundle
- Then a dialogue will appear and fill in the details, then select the release build
- It will take some time and generate an .abb file in {{path}}
- Go to google play console [https://play.google.com/console/u/0/developers](https://play.google.com/console/u/0/developers)
- Go to apps → choose your app → Production Overview → Create Release
- A new page will appear and fill all the fields.
- At the bottom of the page drag & drop the abb file and click on “Rollout to Production”.
- Once the verification is completed it will automatically be published to the Play Store.

### Ios

- Change the environment to prod
- Open Xcode, change version, builder number and the target device to any ios device.
- In the top menu choose product -> clean build folder
- In the top menu select product -> archive (This process will take some time)
- After completing the Archive process, A dialogue will appear, and click the “Distribute App” button.
- Then choose a Release method, choose ”App store connect“ and complete the following steps
- Go to app store connect  [https://play.google.com/console/u/0/developers](https://appstoreconnect.apple.com/login)
- Once the signing process will be over. The app will be uploaded to test flight and available for testing.
- Click on the App Store and create a new version by clicking on the `+` button near iOS App.
- After creating the new version release, fill all the necessary fields and click on *Save* → then `Add for Review`
- After the completion of verification process (it will take approximately 1 day) → developer can manually release the version by login the app store connect.