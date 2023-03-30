---
sidebar_position: 3
---

# Notifications

To implement push notifications in React Native using Firebase, follow these steps:

1. Create a Firebase project:
    - Go to the Firebase console and create a new project.
    - Follow the steps to create a new project and give it a name.

2. Set up Firebase Cloud Messaging (FCM):
    - Go to the Firebase console and select your project.
    - Click on the gear icon and select "Project settings".
    - Go to the "Cloud Messaging" tab.
    - Follow the instructions to configure your FCM project and get the server key.

3. Install the Firebase SDK:
    - In your React Native project, install the Firebase SDK by running the following command
     ```bash
      npm install --save @react-native-firebase/app @react-native-firebase/messaging
     ```

4. Add the Firebase configuration file:
    - Go to the Firebase console and select your project.
    - Click on the gear icon and select "Project settings".
    - Go to the "General" tab.
    - Scroll down to "Your apps" and click on the "Add app" button.
    - Select the "Web" icon.
    - Give your app a nickname and click on the "Register app" button.
    - Copy the Firebase configuration code and paste it into your React Native project.

5. Configure the Firebase SDK
6. Add APN key (iOS only):
    - Go to the Apple Developer portal and create a new APN key.
    - Download the key file and keep it safe.
    - Go to the Firebase console and select your project.
    - Go to the "Cloud Messaging" tab.
    - Click on the "iOS app configuration" button.
    - Upload the APN key file.
    - Enter the APN key ID and team ID.
    - Click on the "Save" button.