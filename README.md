<div align="center">

# New Focus

**Give your life a new focus.**

A cross-platform productivity and wellness app built with Flutter & Firebase: manage tasks, take notes and stay focused, all in one place.

![Flutter](https://img.shields.io/badge/Flutter-02569B?logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-3.1+-0175C2?logo=dart&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-Auth%20%7C%20Firestore-FFCA28?logo=firebase&logoColor=black)
![Riverpod](https://img.shields.io/badge/State-Riverpod%20%2F%20Provider-7C4DFF)
![Platforms](https://img.shields.io/badge/Platforms-Android%20%7C%20iOS%20%7C%20Web%20%7C%20Desktop-4CAF50)
![Status](https://img.shields.io/badge/Status-Beta-orange)

</div>

---

## Table of Contents

- [About](#about)
- [Screenshots](#screenshots)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Author](#author)

## About

**New Focus** is a mobile-first app whose mission is to improve your quality of life by providing tools and resources that make it easier to build healthy habits and optimize your performance in different areas of your life.

This repository contains the complete source code of the app (**Beta**), with a responsive UI that adapts to different devices and screen sizes, and full support for light and dark themes.

## Screenshots

Each screenshot shows two screens side by side: the **welcome + login** flow and the **home** screen with tasks and notes.

### Authentication

<table>
  <tr>
    <th align="center">Dark theme</th>
    <th align="center">Light theme</th>
  </tr>
  <tr>
    <td align="center"><img src="https://github.com/m4icol/App_NewFocus/assets/93083280/6703ac97-a980-40a5-b581-d701f9ffb2ec" alt="Welcome and login screens, dark theme" width="400"></td>
    <td align="center"><img src="https://github.com/m4icol/App_NewFocus/assets/93083280/0c6ffa74-fd4b-4b85-9f41-d0464c1a4a1b" alt="Welcome and login screens, light theme" width="400"></td>
  </tr>
</table>

### Tasks & Notes

<table>
  <tr>
    <th align="center">Dark theme</th>
    <th align="center">Light theme</th>
  </tr>
  <tr>
    <td align="center"><img src="https://github.com/m4icol/App_NewFocus/assets/93083280/f4aaa743-c94a-49f7-b4a7-74304a6624ae" alt="Tasks and notes screens, dark theme" width="400"></td>
    <td align="center"><img src="https://github.com/m4icol/App_NewFocus/assets/93083280/a4972063-a797-41d7-934f-ef0ebb4a9940" alt="Tasks and notes screens, light theme" width="400"></td>
  </tr>
</table>

## Features

- **Authentication**: email/password sign-up and login, Google Sign-In, and password recovery with an OTP verification flow.
- **Onboarding**: animated swipe onboarding (liquid swipe) for first-time users.
- **Tasks**: create tasks with title, description, category, date and time, and mark them as done.
- **Notes**: create, edit and read your notes.
- **Pomodoro timer**: timed work sessions to help you stay focused.
- **Calendar**: date overview powered by `table_calendar`.
- **User profile**: basic profile screen for the signed-in user.
- **Light & dark themes**: carefully designed palettes for both modes.
- **Responsive design**: optimized for different devices and screen sizes.
- **Crash reporting**: Firebase Crashlytics integration.

## Tech Stack

| Area | Technology |
| --- | --- |
| Framework | [Flutter](https://flutter.dev) / Dart (SDK `>=3.1.0`) |
| Backend | Firebase Authentication, Cloud Firestore, Crashlytics |
| Auth providers | Email/password, Google Sign-In |
| State management | [Riverpod](https://riverpod.dev) and Provider |
| UI & charts | `curved_navigation_bar`, `liquid_swipe`, `smooth_page_indicator`, `flutter_otp_text_field`, `fl_chart`, `table_calendar` |
| Local storage | `shared_preferences` |
| Typography | Poppins |
| Platforms | Android, iOS, Web, Windows, macOS, Linux |

## Project Structure

```text
lib/
├── main.dart
├── firebase_options.dart
└── src/
    ├── constants/            # colors, sizes, image strings
    └── features/
        ├── authentication/   # welcome, onboarding, login, signup, forgot password, profile
        └── home/
            └── screens/
                ├── dashboard/
                └── sections/ # header (calendar), tasks, notes, pomodoro
assets/
├── font/                     # Poppins family
└── img/                      # logos, onboarding and emoji assets
```

## Getting Started

### Prerequisites

- [Flutter SDK](https://docs.flutter.dev/get-started/install) (Dart `>=3.1.0`)
- A [Firebase](https://console.firebase.google.com) project
- Android Studio, Xcode or VS Code with the Flutter extension

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/MaickolRivera/newfocus_app.git
cd newfocus_app

# 2. Install dependencies
flutter pub get
```

### Firebase setup

The app uses Firebase Authentication and Cloud Firestore, so you need to connect it to your own Firebase project:

```bash
dart pub global activate flutterfire_cli
flutterfire configure
```

This regenerates `lib/firebase_options.dart` for your project. Then enable **Email/Password** and **Google** sign-in in the Firebase console, and create a Cloud Firestore database.

### Run

```bash
flutter run
```

## Author

Made by **Maickol Rivera** ([@MaickolRivera](https://github.com/MaickolRivera)).

If you like the project, consider giving it a star.
