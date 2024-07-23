Firestore Quickstart
EduQuest is and app built on Firestore. For more information about Firestore visit the [docs](https://firebase.google.com/docs/firestore/).

Getting Started
Set up your Android app for Firestore (https://firebase.google.com/docs/firestore/client/setup-android).
1. Use the package name com.google.firebase.firestore.FirebaseFirestore
In the Authentication tab of the Firebase console (https://console.firebase.google.com/u/0/project/_/authentication/providers) go to the Sign-in Method page and enable 'Email/Password'.
Rename your console as "login-register-eduquest".
Run the app on an Android device or emulator.

Security Rules
Add the following security rules to your project in the: rules tab:
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if request.auth != null;
      }
   }
}

Run the App
When you open the app you will be prompted to sign in, choose any email and password by follow the on-screen instructions.
