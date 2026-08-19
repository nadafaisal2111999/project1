# 📝 Taskatii - Task Management App

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)
![Hive](https://img.shields.io/badge/Hive-Local%20Storage-orange?style=for-the-badge)

A modern, simple, and clean Task Management application built using **Flutter** and **Dart**. Designed to help users organize daily tasks and manage to-do lists through an intuitive user interface.

---

## ✨ Features

* 🎨 **Clean & Modern UI:** Designed with a smooth purple theme and clean card layouts.
* ➕ **Task Creation:** Create new tasks with custom titles and detailed descriptions.
* 🗑️ **Delete Tasks:** Instantly remove tasks with a dedicated action button.
* 💾 **Local Data Persistence:** Keeps all task data saved locally on the device using Hive.

---

## 📸 Screenshots

| Main Screen |
| :---: |
| <img src="screenshots/home.png" width="260"/> |

> *Note: Place your screenshot in a `screenshots` folder in the project root and name it `home.png`.*

---

## 🗺️ Roadmap & Upcoming Features

- [x] Basic Task Creation & Deletion
- [x] Clean Card Layout & Purple Theme Setup
- [x] Local Persistence Setup
- [ ] ⏳ Input Validation (Prevent empty task submissions)
- [ ] ⏳ Mark Tasks as Completed (Checkmark toggle)
- [ ] ⏳ Edit Existing Tasks
- [ ] ⏳ Add User Profile Avatar to Header

---

## 💡 Challenges & Problem Solving

### Schema Conflict in Local Storage During Testing
* **Problem:** The app crashed during startup due to a data parsing error when retrieving cached tasks from local storage.
* **Root Cause:** A schema mismatch occurred between old legacy cached test data and the updated Model structure during rapid development iterations.
* **Solution:** Programmatically cleared the local disk storage cache (`Hive.deleteBoxFromDisk`) during bootstrapping to re-initialize the storage with the newly updated schema structure smoothly.

---

## 🛠️ Tech Stack & Dependencies

* **Framework:** Flutter
* **Language:** Dart
* **Local Storage:** Hive (`hive`, `hive_flutter`)
* **Icons:** `cupertino_icons`

---

## 📂 Project Structure

```text
lib/
├── models/         # Task data model & Hive type adapters
├── screens/        # Main task screen & UI components
├── widgets/        # Custom card widgets & floating buttons
└── main.dart       # App entry point & storage initialization
