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
| <img width="1237" height="2257" alt="Screenshot 2026-08-20 003223" src="https://github.com/user-attachments/assets/2c38c3a2-f87e-46d1-bc45-6b8ad2fa7929" />
 |
 <img width="1232" height="2237" alt="Screenshot 2026-08-20 003242" src="https://github.com/user-attachments/assets/143bac28-8010-4a5c-88ee-bb257ae029e2" />

<img width="1255" height="2265" alt="Screenshot 2026-08-20 003308" src="https://github.com/user-attachments/assets/a1b3d356-f9b8-41fc-a77e-29db1ae116ce" />


> *Note: Place your screenshot in a `screenshots` folder in the project root and name it `home.png`.*

---

## 🗺️ Roadmap & Upcoming Features

- [x] Basic Task Creation & Deletion
- [x] Clean Card Layout & Purple Theme Setup
- [x] Local Persistence Setup (Hive)
- [x] Form Validation (Prevent empty task submission)
- [x] Mark Task as Completed (Checkmark toggle)
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
