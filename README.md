# Task Manager App

Simple Android task app built with Kotlin and Jetpack Compose.

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