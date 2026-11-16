# Experiment 3: Flexible UI with Fragments and Debugging

This project demonstrates how to build a modern, adaptive Android application using Fragments and advanced debugging techniques in Android Studio.

## 🚀 Project Overview

The application implements a **Master-Detail flow** that displays a list of items (Courses, Products, etc.) and their corresponding details. It is designed to be **adaptive**, meaning the UI automatically adjusts based on the device's screen size.

## 📸 Screenshots

### 1) Main list screen
![Main list screen](Screenshot%20(343).png)

### 2) Kotlin detail screen
![Kotlin detail screen](Screenshot%20(344).png)

### 3) Fragments detail screen
![Fragments detail screen](Screenshot%20(345).png)

### Key Features
- **Adaptive UI**: Uses `SlidingPaneLayout` to show a two-pane layout on large screens (tablets/foldables) and a single-pane layout on small screens (phones).
- **Fragment Management**: Utilizes `ListFragment` and `DetailFragment` for modular and reusable UI components.
- **Modern Architecture**: Built with Kotlin and Jetpack libraries like `RecyclerView` and `FragmentContainerView`.

---

## 🛠️ Concepts Explored

### 1. Fragments
Fragments represent a reusable portion of your app's UI. They have their own lifecycle and can be combined into a single Activity.
- **ListFragment**: Handles the logic for displaying the `RecyclerView`.
- **DetailFragment**: Receives data via Arguments and displays detailed information.

### 2. Adaptive UI with SlidingPaneLayout
Instead of creating separate layouts for phone and tablet, we use `SlidingPaneLayout`. 
- On **large screens**, it displays both fragments side-by-side.
- On **small screens**, it hides the detail pane behind the list, allowing users to swipe or click to reveal it.

### 3. RecyclerView & Adapters
Efficiently displays long lists of data. The `ItemAdapter` maps our `Item` data class to the XML view.

---

## 🐞 Debugging Tasks

A major focus of this experiment was using Android Studio's debugging tools to analyze program execution.

### Normal Breakpoint
- **Location**: `DetailFragment.kt` inside `onViewCreated`.
- **Purpose**: To observe the Fragment lifecycle, check local variable values, and inspect the Call Stack to see how the code was executed.

### Conditional Breakpoint
- **Location**: `ItemAdapter.kt` inside the click listener.
- **Condition**: `item.name == "Android"`
- **Purpose**: To pause execution only when a specific data condition is met, saving time during complex debugging sessions.

---

## 📖 How to Run

1. Clone the repository.
2. Open the project in **Android Studio (Ladybug or later)**.
3. Sync the project with Gradle.
4. Run the app on an emulator or physical device.
5. To test debugging, click the **Bug icon** in the toolbar.

---

## 📂 Project Structure

- `MainActivity.kt`: The entry point that orchestrates the fragments.
- `ListFragment.kt`: Displays the item list.
- `DetailFragment.kt`: Displays item details.
- `Item.kt`: Data model.
- `ItemAdapter.kt`: RecyclerView adapter with click handling.
- `activity_main.xml`: Contains the `SlidingPaneLayout`.
