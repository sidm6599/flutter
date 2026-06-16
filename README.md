# Flutter Firebase Login

A simple Flutter application that demonstrates user authentication using **Firebase**. It supports email/password sign-up and sign-in, as well as **Google Sign-In**, and shows a personalized home screen for the logged-in user.

## ✨ Features

- 📝 **Sign Up** with name, email and password (with form validation)
- 🔐 **Sign In** with email and password
- 🟦 **Google Sign-In** integration
- 👤 **Home screen** showing the logged-in user's name, email and profile photo
- 🔄 Automatic auth-state handling — users are routed to the right screen based on whether they are signed in
- 🚪 **Log out** support

## 📱 Screens

| Screen | Description |
| --- | --- |
| **Sign In** | Email/password login, Google Sign-In button, link to Sign Up |
| **Sign Up** | Create a new account with name, email and password |
| **Home** | Greets the user, shows avatar (Google photo or default asset), and a Log Out button |

## 🛠️ Tech Stack

- [Flutter](https://flutter.dev/) (Dart)
- [Firebase Authentication](https://firebase.google.com/docs/auth) — `firebase_auth`
- [Google Sign-In](https://pub.dev/packages/google_sign_in) — `google_sign_in`
- [Flutter Auth Buttons](https://pub.dev/packages/flutter_auth_buttons) — `flutter_auth_buttons`

## 📂 Project Structure

```
lib/
├── main.dart        # App entry point, theme & named routes (/home, /signin, /signup)
├── HomePage.dart    # Home screen for authenticated users
├── SignIn.dart      # Email/password + Google sign-in screen
└── SignUp.dart      # New account registration screen
asset/
└── index.png        # Default avatar / logo image
```

## 🚀 Getting Started

### Prerequisites

- [Flutter SDK](https://docs.flutter.dev/get-started/install) installed
- An Android/iOS emulator or a physical device
- A [Firebase](https://console.firebase.google.com/) project

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/sidm6599/flutter.git
   cd flutter
   ```

2. **Install dependencies**
   ```bash
   flutter pub get
   ```

3. **Set up Firebase**
   - Create a project in the [Firebase Console](https://console.firebase.google.com/).
   - Enable **Email/Password** and **Google** sign-in providers under **Authentication → Sign-in method**.
   - Add an Android app and download `google-services.json`, then place it in `android/app/`.
   - (iOS) Add an iOS app and download `GoogleService-Info.plist` into `ios/Runner/`.
   - Make sure the Google Services Gradle plugin is applied in your `android/build.gradle` and `android/app/build.gradle`.

4. **Run the app**
   ```bash
   flutter run
   ```

## 📝 Notes

- This project uses the legacy `firebase_auth` API (`FirebaseUser`, `AuthResult`, `onAuthStateChanged`). If you are on a newer Flutter/Firebase version, the API names may differ (`User`, `UserCredential`, `authStateChanges()`).
- Remember to register your app's **SHA-1** fingerprint in Firebase for Google Sign-In to work on Android.

## 👤 Author

**Siddhesh Mishra** — [@sidm6599](https://github.com/sidm6599)

---

*Educational project demonstrating Firebase authentication in Flutter.*
