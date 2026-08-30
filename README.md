# <img width="30" height="30" alt="logo_light" src="assets/screenshots/logo_light.png" /> Grades

A Flutter app for tracking GPA, and monitoring academic progress in real time, with full offline support.

<p align="center">
  <img width="3972" height="1929" alt="frame" src="assets/screenshots/frame.png" />
</p>

---

## 🔗 Links

* 📱 Download App: [Play Store](https://play.google.com/store/apps/details?id=com.iniunamid.scholr)
<!-- * 🎥 Demo Video: [Add video link] -->

---

## 🚀 Key Capabilities

* Supports multiple and custom grading scales (4.0, 4.3, 5.0, etc.)
* Custom letter grade mappings per institution
* Weighted GPA calculations across semesters
* Automatic grouping of semesters into academic years
* Shared core logic powering both mobile and admin apps
<!--* Target grade simulation to reach a desired CGPA -->

---

## 💡 Engineering Decisions

### Shared Core Engine (`grades_core`)

* **What:** Extracted all GPA logic and domain models into a pure Dart package
* **Why:** Keeps business logic separate from UI and allows reuse across mobile and admin apps without duplication

### Store + ViewModel Pattern

* **What:** Centralized Stores handle realtime data, while ViewModels manage screen logic
* **Why:** Keeps UI clean and separates global app state from temporary screen state

### Network-Aware ViewModel

* **What:** Connectivity checks and UI events handled inside `BaseViewModel`
* **Why:** Prevents failed requests and provides consistent handling for errors, toasts, and retries

---

## 🧪 Production Readiness

* Offline-first experience using Firestore caching
* Realtime updates with snapshot listeners
* Network-aware write protection
* Crash tracking with Firebase Crashlytics
* Remote Config for feature flags and updates without redeploying

---

## 📦 Architecture

* `grades_app` → Flutter mobile client
* `grades_admin` → Admin dashboard
* `grades_core` → Shared business logic and models

```text
grades/
 ├── grades_app/
 ├── grades_admin/
 └── grades_core/
```

This structure keeps logic reusable, testable, and independent from UI layers.

---

## 📱 Gallery

<p align="center">
  <img alt="home-stats-portrait" src="assets/screenshots/home-portrait.png" width="180" style="margin: 6px;"/>
  <img alt="academics-portrait" src="assets/screenshots/academics-portrait.png" width="180" style="margin: 6px;"/>
  <img alt="account-portrait" src="assets/screenshots/account-portrait.png" width="180" style="margin: 6px;"/>
  <img alt="profile-portrait" src="assets/screenshots/profile-portrait.png" width="180" style="margin: 6px;"/>
</p>

<p align="center">
  <img alt="search-portrait" src="assets/screenshots/search-portrait.png" width="180" style="margin: 6px;"/>
  <img alt="edit-course-portrait" src="assets/screenshots/edit-course-portrait.png" width="180" style="margin: 6px;"/>
  <img alt="year-details-portrait" src="assets/screenshots/year-details-portrait.png" width="180" style="margin: 6px;"/>
  <img alt="semester-deets-portrait" src="assets/screenshots/semester-deets-portrait.png" width="180" style="margin: 6px;"/>
</p>
