# My Workout Tracker (Android)

An offline-first Android app for the Monday–Sunday beginner workout plan. Daily checkmarks and weekly progress are stored locally on the device using WebView local storage. No account or internet connection is required.

## Build an APK with Android Studio

1. Install Android Studio (current stable) and its Android SDK Platform 35.
2. Open this folder in Android Studio: `MyWorkoutTracker`.
3. Allow Android Studio to sync/download the Gradle and Android Gradle Plugin dependencies.
4. Select **Build → Build Bundle(s) / APK(s) → Build APK(s)**.
5. When the build finishes, choose **locate**. The debug APK is at:
   `app/build/outputs/apk/debug/app-debug.apk`
6. Transfer the APK to your Android phone and open it. If Android asks, allow installation from that source.

For a signed release APK, use **Build → Generate Signed Bundle / APK → APK** and follow the signing wizard.

## Requirements

- Android Studio with JDK 17 or newer
- Android SDK Platform 35
- Gradle 8.9 or compatible version downloaded by Android Studio
- Minimum Android version: Android 6.0 (API 23)

## App details

- App name: My Workout Tracker
- Package: `com.nok.workouttracker`
- Version: 1.0
- Orientation: portrait
- Offline operation: yes
- Progress storage: local to the app on the phone; clearing app data or uninstalling the app can erase it.

## Workout plan included

- Monday: squats, push-ups, glute bridges, plank
- Tuesday: brisk walk, 20–30 minutes
- Wednesday: lunges, incline push-ups, backpack rows, plank
- Thursday: brisk walk, 20–30 minutes
- Friday: squats, push-ups, backpack rows, glute bridges
- Saturday: brisk walk, 20–30 minutes
- Sunday: rest and recovery

The project uses a local HTML interface inside a minimal Android WebView shell. It requests no internet permission and includes no analytics or advertising.

## Build in GitHub Actions (without installing Android Studio locally)

This project includes `.github/workflows/build-apk.yml`.

1. Create a GitHub repository and upload the contents of this project.
2. Open the repository's **Actions** tab.
3. Run **Build Android APK** using **Run workflow** (or push to the `main` branch).
4. When the workflow succeeds, open the run and download the `MyWorkoutTracker-debug-apk` artifact.
5. Extract the artifact ZIP; it contains `app-debug.apk`. Transfer that APK to your Android phone and install it.
