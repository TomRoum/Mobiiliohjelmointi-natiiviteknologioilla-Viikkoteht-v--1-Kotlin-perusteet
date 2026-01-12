# Task Manager App

Simple Android task app built with Kotlin and Jetpack Compose.

**📦 [Download APK (v1.0)](https://github.com/TomRoum/Mobiiliohjelmointi-natiiviteknologioilla-Viikkoteht-v--1-Kotlin-perusteet/releases/tag/v1.0)**

## Getting Started

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd MyApplication
   ```

2. **Open in Android Studio**
    - Open Android Studio
    - Select "Open an Existing Project"
    - Navigate to the cloned folder and click OK

3. **Sync Gradle**
    - Android Studio will prompt you to sync
    - Click "Sync Now" or click the elephant icon 🐘 in the toolbar

4. **Run the app**
    - Connect an Android device or start an emulator
    - Click the green play button ▶️
    - Select your device and click OK

## Data Model

**Task** data class with: id, title, description, priority, dueDate, done

Mock data contains 6 sample tasks.

## Functions

All functions return new lists (immutable/functional style):

- **addTask(list, task)** - adds task to end of list
- **toggleDone(list, id)** - flips task done status (true ↔ false)
- **filterByDone(list, done)** - returns only tasks matching done status
- **sortByDueDate(list)** - sorts tasks by due date (earliest first)

## UI

**HomeScreen** displays tasks with buttons to test each function.

## Structure

```
MainActivity.kt (modified to use HomeScreen)
domain/
  ├── Task.kt
  ├── MockData.kt
  └── TaskFunctions.kt
ui/
  └── HomeScreen.kt
```