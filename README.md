# Flutter Firebase Push

A simple Flutter App connected to Firebase that receives messages.

## Getting Started

Create Firebase project and update app config:

1. Access [Firebase Console](https://console.firebase.google.com) and create a new project.
2. In the "Cloud Messaging" blade select to add an "Android" app.
3. Give it a package name `com.example.flutter_azure_push` (must match `AndroidManifest.xml`).
4. Register the app.
5. Download and copy the `google-services.json` file to the Android `app` directoy.
6. Add dependencies *(not needed for this project, already set up)*.

## Running the app

After the setup, run the app:

1. Connect your device.
2. `flutter packages get`
3. `flutter run`

## Test in Firebase

1. Copy the device token from the console output.
2. Go to the Firebase Console and select "Send your first message".
3. Set title and body texts.
4. Create test message, and add the device token.
5. Select the App.
6. Review and publish message.

Your Flutter App should be updated with the message received.

## Azure Notification Hub

Possibility to send push via Azure Notification Hub.

1. Creat a resource group and the notification hub ([Template](https://azure.microsoft.com/en-us/resources/templates/101-notification-hub/)).
2. Copy the `Server Key` from the Firebase Console.
3. Paste into **Google (GCM/FCM)** blade **API Key** field.
4. Test/Send via the Portal option


## References

https://firebase.google.com/docs/android/setup?authuser=0

https://pub.dev/packages/firebase_messaging

https://github.com/flutter/plugins/tree/master/packages/firebase_messaging
