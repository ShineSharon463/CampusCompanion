# 🏫 Campus Companion

A modern, responsive, and cross-platform mobile application built with **React Native (Expo CLI)** designed to help students manage daily campus life efficiently. This application showcases complex nested navigation architectures, advanced form validation, platform-specific adaptations, and clean state management practices.

---

## 📘 Project Overview

**Campus Companion** acts as a centralized dashboard for students to track ongoing university events, jot down quick academic notes, access essential web links, and manage their student profile. 

This project serves as a comprehensive demonstration of core React Native mechanics, focusing heavily on standard routing architectures, UI responsiveness, performance hooks, and cross-platform native API interactions.

---

## 🎨 UI Architecture & Navigation Flow

The app integrates a multi-tier nested navigation structure using `@react-navigation`:

```text
├── 🧭 Drawer Navigation (Main Container)
│   ├── 🏠 Home (Hosts Bottom Tab Navigator)
│   │   ├── 📰 Feed (Campus Updates & Quick Links)
│   │   └── 📝 Notes (Interactive Note Logger)
│   ├── 📅 Events (Hosts Stack Navigator)
│   │   └── 🔍 Event Details (With custom screen transition animations)
│   ├── 👤 Profile (User data configuration)
│   └── ⚙️ Settings (Application configurations)
```

---

## ⚙️ Technologies & Tools Used

| Tool / Library | Purpose & Implementation Details |
| :--- | :--- |
| **React Native (Expo CLI)** | Framework for cross-platform Android & iOS deployment. |
| **TypeScript / JavaScript** | App logic layer implementing robust type safety and clean coding practices. |
| **@react-navigation/native** | Core routing foundation managing overall app screen states. |
| **Hooks (`useState`, `useEffect`, `useRef`)** | Functional state tracking, side-effect simulation, and direct element referencing. |
| **Platform Module** | Executes native platform feedback: `Toast` messages on Android, `Alert` dialogs on iOS. |
| **Flexbox & StyleSheet** | UI layout framework using performance-optimised, modular style sheets. |

---

## 🧩 Features Implemented

* 🧭 **Multi-Tier Navigation Hierarchy:** Seamlessly combines Drawer, Bottom Tab, and Stack routing paradigms into a singular cohesive user experience.
* 🧭 **Dynamic Layout Engine:** Automatically flips between 1-column and 2-column feed layouts depending on live screen aspect ratios and dimensions.
* 📝 **Safe Note Validation Subsystem:** Hardened text processing forms that dynamically validate entries, toggle interactive submission states, and provide concrete persistence feedback.
* 📅 **Simulated Microservice Fetching:** Utilizes async timers within functional side-effects to simulate network activity, rendering distinct loading layouts during operations.
* 🕒 **Deterministic Hybrid Components:** Houses a standalone `LegacyClock` class component explicitly designed to showcase clean lifecycle tracking (`componentDidMount` / `componentWillUnmount`) without memory leaks.

---

## 🏗️ Project Folder Structure

```text
CampusCompanion/
├── App.js                         # Application entrypoint & root navigation provider
├── assets/                        # Static local media, iconography, and image assets
├── components/                    # Reusable visual layout atoms
│   ├── LegacyClock.js             # Classic lifecycle clock component
│   ├── NoteItem.js                # Render card for note entry data 
│   └── QuickLinkItem.js           # Interactive button for quick web navigation
├── data/                          # Mock relational database files (.json)
│   ├── events.json
│   └── links.json
├── hooks/                         # Optimized custom hook extractions
│   └── useFetchEvents.js          # Async simulated data service state manager
├── navigation/                    # Structural routing modules
│   ├── DrawerNavigator.js         # Top-level global navigation shell
│   ├── EventsStack.js             # Detailed event screen stack provider
│   └── HomeTabs.js                # Core homepage tab distributor
└── screens/                       # Target landing views
    ├── EventDetailsScreen.js
    ├── EventsScreen.js
    ├── FeedScreen.js
    ├── NotesScreen.js
    ├── ProfileScreen.js
    └── SettingsScreen.js
```

---

## 💻 Project Setup & Execution

Follow these steps to spin up the codebase locally:

### 1. Global Setup
Ensure you have the Expo CLI tooling configured globally:
```bash
npm install -g expo-cli
```

### 2. Dependency Resolution
Navigate to your project root folder and install required navigation infrastructure and core native dependencies:
```bash
npm install @react-navigation/native @react-navigation/drawer @react-navigation/bottom-tabs @react-navigation/stack prop-types

npx expo install react-native-screens react-native-safe-area-context react-native-gesture-handler react-native-reanimated
```

### 3. Initialize Runtime
Boot up the local Metro Bundler:
```bash
npx expo start
```
* Press **`a`** to inject the application directly into a running local Android Virtual Device (AVD).
* Scan the displayed terminal QR code inside the **Expo Go** application on your physical smartphone to preview live code hot-swapping instantly.

---

## 🏁 Conclusion

The Campus Companion project provides a scalable template demonstrating how to bind disparate mobile architectures under a single React Native application context. Through its strict adherence to atomic component structures, native platform API forks, and resilient runtime hooks, the project provides a rock-solid foundation for modular native applications.
