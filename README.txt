# PracticePort – Android Wellness Tracker App

PracticePort is a Kotlin-based Android mobile application designed to help users manage daily wellness activities through habit tracking, mood journaling, hydration tracking, reminders, progress visualization, and local data storage.

The project focuses on Android mobile application development using Kotlin, XML layouts, Material Design components, SharedPreferences, WorkManager, charts, fragments, bottom navigation, and a home screen widget.

## Features

* Splash screen with app launch animation
* Onboarding flow with wellness feature introduction
* Login and registration screens with input validation
* Remember-me option for login email
* Main dashboard with bottom navigation
* Daily habit tracking
* Add, update, complete, and delete habits
* Habit frequency support: Daily, Weekly, and Monthly
* Habit categories such as Focus, Fitness, Rest, Learning, Health, and General
* Habit progress visualization using charts
* Mood journal with emoji-based mood selection
* Mood notes and mood history
* Mood calendar view
* Mood trend visualization using MPAndroidChart
* Hydration tracker
* Daily water intake goal tracking
* Custom water intake entries
* Hydration progress chart
* Hydration reminders using WorkManager
* Mood check-in reminders using WorkManager
* Notification settings
* Dark mode setting toggle
* Data export as text using Android share intent
* Reset all local app data
* Home screen widget for habit progress
* Responsive layout support for larger screens

## Technologies Used

* Kotlin
* Android Studio
* Android XML Layouts
* Material Design Components
* SharedPreferences
* WorkManager
* MPAndroidChart
* RecyclerView
* ViewPager2
* BottomNavigationView
* AppWidgetProvider
* Gradle Kotlin DSL

## Project Structure

```text
PracticePort/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/example/habitmate/
│   │   │   │   ├── data/
│   │   │   │   │   ├── DataManager.kt
│   │   │   │   │   └── Models.kt
│   │   │   │   ├── onboarding/
│   │   │   │   ├── ui/
│   │   │   │   │   ├── auth/
│   │   │   │   │   ├── home/
│   │   │   │   │   ├── hydration/
│   │   │   │   │   ├── mood/
│   │   │   │   │   ├── settings/
│   │   │   │   │   └── splash/
│   │   │   │   ├── utils/
│   │   │   │   └── widget/
│   │   │   └── res/
│   │   │       ├── drawable/
│   │   │       ├── layout/
│   │   │       ├── layout-sw600dp/
│   │   │       ├── menu/
│   │   │       ├── values/
│   │   │       └── xml/
│   └── build.gradle.kts
├── build.gradle.kts
├── settings.gradle.kts
└── README.md
```

## Main Modules

### 1. Authentication

The app includes login and registration screens with form validation for name, email, password, and confirm password. User details are saved locally using SharedPreferences.

### 2. Onboarding

PracticePort includes a multi-screen onboarding flow that introduces the main wellness features of the app, including habit tracking, mood tracking, and hydration tracking.

### 3. Habit Tracker

The habit tracker allows users to create and manage habits with name, description, frequency, category, completion status, streaks, and progress tracking.

### 4. Mood Journal

The mood journal allows users to record daily mood entries using emoji-based mood types. Users can add notes, view mood history, use the calendar view, and analyze mood trends with charts.

### 5. Hydration Tracker

The hydration section helps users track daily water intake, set hydration goals, add custom intake amounts, view hydration progress, and enable reminder notifications.

### 6. Settings

The settings section includes user information, notification settings, dark mode toggle, data export, reset data, about dialog, and logout functionality.

### 7. Home Screen Widget

The app includes a home screen widget that displays today’s habit completion progress and allows quick access back to the app.

## Local Data Storage

This project uses SharedPreferences for local data storage. It does not use Firebase, an external database, or a backend server.

Stored data includes:

* User profile details
* Habit data
* Habit completion entries
* Mood journal entries
* Hydration data
* Notification settings
* User preferences
* Achievement data

## How to Run the Project

1. Clone the repository:

```bash
git clone https://github.com/Anuradha-dol/practiceport-android-wellness-tracker.git
```

2. Open the project in Android Studio.

3. Let Android Studio sync the Gradle files.

4. Connect an Android device or start an emulator.

5. Click **Run** to launch the app.

## Requirements

* Android Studio
* Kotlin
* Android SDK
* Minimum SDK: 24
* Target SDK: 36

## Dependencies

Main dependencies used in this project:

* AndroidX Core KTX
* AndroidX AppCompat
* Material Components
* ConstraintLayout
* Fragment KTX
* Navigation Fragment KTX
* Navigation UI KTX
* WorkManager
* MPAndroidChart
* ViewPager2
* RecyclerView
* CardView

## Project Purpose

The purpose of this project was to improve Android mobile application development skills by building a wellness-focused app with local data handling, modern UI design, fragments, navigation, charts, reminders, and widget integration.

## Author

Anuradha Dolamulla

GitHub: https://github.com/Anuradha-dol
