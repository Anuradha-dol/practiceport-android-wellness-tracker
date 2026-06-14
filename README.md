# PracticePort

PracticePort is a native Android wellness tracker built with Kotlin. It brings habit tracking, mood journaling, hydration tracking, reminder notifications, simple analytics, and a home screen widget into one local-first mobile app.

The project is designed as a practical Android development assignment, with the main focus on Kotlin, XML layouts, Material Design components, local persistence, background work, charts, and responsive UI behavior.

## Project Document

The project overview and UI screenshots are available here:

[Project overview and UI screenshots](docs/project-overview-and-ui-screenshots.pdf)

## What the App Does

- Guides first-time users through a three-step onboarding flow.
- Provides local login and registration screens with form validation.
- Tracks daily habits with add, edit, complete, and delete actions.
- Shows habit progress using a progress bar, summary statistics, and a pie chart.
- Records mood entries with mood selection, notes, history, calendar view, sharing, editing, and deletion.
- Displays mood trends using MPAndroidChart line charts.
- Tracks hydration progress using custom water intake amounts and daily goals.
- Supports hydration reminders through WorkManager and exact-time alarm scheduling.
- Supports mood check-in reminders through WorkManager.
- Includes settings for notifications, dark mode preference, data export, reset, about, and logout.
- Provides a home screen widget for today's habit completion percentage.
- Includes tablet-aware layout support through `layout-sw600dp`.

## App Flow

1. `SplashActivity` launches the app with animated branding.
2. New users are sent to onboarding unless it has already been completed.
3. Users register or log in through the local authentication screen.
4. `MainActivity` hosts the main bottom navigation experience:
   - Home
   - Mood
   - Hydration
   - Settings

## Tech Stack

| Area | Implementation |
| --- | --- |
| Language | Kotlin |
| UI | Android XML layouts, ViewBinding, Material Components |
| Navigation | Fragment-based screen switching with BottomNavigationView |
| Local storage | SharedPreferences with JSON serialization |
| Charts | MPAndroidChart |
| Background work | WorkManager |
| Notifications | Android notification channels and pending intents |
| Widget | AppWidgetProvider and RemoteViews |
| Build system | Gradle Kotlin DSL |

## Project Details

| Item | Value |
| --- | --- |
| App name | PracticePort |
| Application ID | `com.example.habitmate` |
| Minimum SDK | 24 |
| Target SDK | 36 |
| Compile SDK | 36 |
| Version | 1.0 |

## Main Features

### Habit Tracking

The home screen acts as the habit dashboard. Users can create habits, set a frequency, mark today's progress, edit existing habits, and remove habits when needed. The dashboard also shows total active habits, current streak information, best streak information, and a visual completion chart.

### Mood Journal

The mood module lets users record how they feel for a specific day, attach an optional note, and view previous entries. It includes a monthly calendar view, a seven-day trend chart, entry details, edit/delete actions, and Android share intent support for mood entries.

### Hydration Tracker

The hydration module tracks daily intake against a configurable goal. Users can add predefined or custom water amounts, update the daily goal, set reminder intervals, schedule an exact reminder time, view a weekly bar chart, and reset the current day's hydration data.

### Reminders and Notifications

Hydration and mood reminders are scheduled with WorkManager. Hydration also supports exact-time reminders through AlarmManager where the device allows exact alarms. Notification settings can be managed from the Settings screen.

### Local Data Management

The app stores data locally with SharedPreferences. There is no Firebase, external database, backend API, or cloud sync layer in the current version.

Stored data includes:

- User profile details
- Habits and daily completion entries
- Mood journal entries
- Hydration goal and progress
- Notification preferences
- User preferences
- Achievement and analytics-related data models

## Folder Structure

```text
practiceport-android-wellness-tracker/
|-- app/
|   |-- src/main/
|   |   |-- java/com/example/habitmate/
|   |   |   |-- MainActivity.kt
|   |   |   |-- data/
|   |   |   |   |-- DataManager.kt
|   |   |   |   `-- Models.kt
|   |   |   |-- onboarding/
|   |   |   |-- ui/
|   |   |   |   |-- auth/
|   |   |   |   |-- home/
|   |   |   |   |-- hydration/
|   |   |   |   |-- mood/
|   |   |   |   |-- settings/
|   |   |   |   `-- splash/
|   |   |   |-- utils/
|   |   |   `-- widget/
|   |   `-- res/
|   |       |-- drawable/
|   |       |-- layout/
|   |       |-- layout-sw600dp/
|   |       |-- menu/
|   |       |-- values/
|   |       `-- xml/
|   `-- build.gradle.kts
|-- docs/
|   `-- project-overview-and-ui-screenshots.pdf
|-- gradle/
|-- build.gradle.kts
|-- settings.gradle.kts
`-- README.md
```

## Requirements

- Android Studio
- Android SDK with API 36 installed
- JDK 11 or compatible Android Studio runtime
- Android device or emulator running API 24 or higher

## Running the Project

Clone the repository:

```bash
git clone https://github.com/Anuradha-dol/practiceport-android-wellness-tracker.git
```

Open the project in Android Studio, let Gradle sync complete, then run the `app` configuration on an emulator or Android device.

You can also check the build from the terminal:

```bash
./gradlew assembleDebug
```

On Windows PowerShell:

```powershell
.\gradlew.bat assembleDebug
```

## Permissions Used

- `POST_NOTIFICATIONS` for hydration and mood reminders on newer Android versions.
- `WAKE_LOCK` for background reminder work.
- `RECEIVE_BOOT_COMPLETED` for reminder-related system behavior.
- `SCHEDULE_EXACT_ALARM` for exact-time hydration reminders where supported.

## Current Scope

PracticePort is a local-first student project. Authentication is handled locally for demonstration purposes, and social sign-in/import actions are present as UI placeholders. The app is suitable for demonstrating Android UI development, local storage, charts, reminders, widgets, and wellness-focused mobile workflows.

## Author

Anuradha Dolamulla

GitHub: [Anuradha-dol](https://github.com/Anuradha-dol)
