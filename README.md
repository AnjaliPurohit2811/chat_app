# 🗨️ Chat Application
A simple chat application built with Flutter and Firebase, supporting real-time messaging, authentication, and push notifications using Firebase services.

## 🚀 Features
### Firebase Authentication: User sign-in and sign-up with email and password.
### Real-Time Messaging: Chat with real-time updates using Firebase Firestore.
### Push Notifications: Receive notifications for new messages via Firebase Cloud Messaging (FCM).

## 🛠️ Tech Stack
### Framework: Flutter
### Backend: Firebase (Authentication, Firestore, Cloud Messaging)
### State Management: Getx
## ⚙️ Firebase Setup
1. Create Firebase Project
Go to Firebase Console and create a new project.
Add your Android and/or iOS app to the Firebase project.
Download and add the Firebase configuration files:
google-services.json for Android: Place in android/app/.
GoogleService-Info.plist for iOS: Place in ios/Runner/.
2. Enable Firebase Services
Authentication: Go to Firebase Console > Authentication > Sign-in method > Enable Email/Password.
Firestore Database: Set up a Firestore database in production or test mode.
Firebase Cloud Messaging: Enable FCM for push notifications.
📝 Installation

1. Clone the Repo
```
bash
Copy code
git clone https://github.com/yourusername/chat-app.git
cd chat-app
```
2. Install Dependencies
 ```
bash
Copy code
flutter pub get
```
4. Run the App
Ensure you have an emulator running or a physical device connected, then run:
```

bash
Copy code
flutter run
```
🔥 Firebase Integration
Firebase Authentication
Manages user registration and login via firebase_auth.
Provides basic email/password authentication.
dart
```
Copy code
FirebaseAuth.instance.createUserWithEmailAndPassword(email: email, password: password);
```
Firebase Firestore
Stores and retrieves real-time messages.
Messages are stored in a chats collection with fields like senderId, message, and timestamp.
dart
```
Copy code
FirebaseFirestore.instance.collection('chats').add({
  'senderId': senderId,
  'message': message,
  'timestamp': FieldValue.serverTimestamp(),
});
```
Firebase Cloud Messaging (FCM)
Push notifications alert users of new messages, even when the app is in the background or closed.
dart
```
Copy code
FirebaseMessaging.onMessage.listen((RemoteMessage message) {
  // Handle in-app message notifications
});
```

## 📁 Project Structure
```
bash
Copy code
lib/
├── main.dart              # App entry point
├── services/              # Firebase services
│   ├── auth_service.dart   # Authentication service
│   └── chat_service.dart   # Chat functionality
├── models/                # Data models
│   └── user.dart           # User model
├── screens/               # UI screens
│   ├── login_screen.dart   # Login screen
│   ├── chat_screen.dart    # Chat screen
│   └── profile_screen.dart # User profile screen
└── widgets/               # Reusable UI components
```
## 📦 Dependencies
yaml
```
Copy code
dependencies:
  flutter:
    sdk: flutter
  firebase_core: latest_version
  firebase_auth: latest_version
  cloud_firestore: latest_version
  firebase_messaging: latest_version
```
## ✨ Firebase Packages Used
```
firebase_core: Initializes Firebase.
firebase_auth: Authentication services.
cloud_firestore: Firestore database.
firebase_messaging: Push notifications.
```

## ScreenShot

<p align='center'>
  <img src='https://github.com/user-attachments/assets/509ed966-95c2-4493-9c30-025748da3b35' width=240>
  <img src='https://github.com/user-attachments/assets/8f4fdc6a-3d0e-49c1-8a11-a6656a303bc9' width=240>
  <img src='https://github.com/user-attachments/assets/a5e8a84c-0b15-443c-abdc-0f49821288cd' width=240>
  <img src='https://github.com/user-attachments/assets/67043188-d9c6-4b8b-bdc6-1a02d8c54be0' width=240>
  <img src='https://github.com/user-attachments/assets/11647639-9cfc-4410-a510-4502f4a80ef6' width=240>
  <img src='https://github.com/user-attachments/assets/61cf4fe1-5dbd-4e8b-a55b-32c1c23548b0' width=240>


</p>

## Video

https://github.com/user-attachments/assets/5478662f-1708-407f-9be0-27407060b768


