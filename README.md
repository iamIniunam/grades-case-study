# <img width="30" height="30" alt="logo_light" src="https://github.com/user-attachments/assets/0700e1ec-fe1b-4963-ab9c-ebedc405835a" /> Grades

A Flutter app for tracking GPA, and monitoring academic progress in real time, with full offline support.

<p align="center">
  <img width="3972" height="1929" alt="frame" src="https://github.com/user-attachments/assets/c225fe51-c3bf-4179-9b88-f297143c65f9" />
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
  <img alt="home-stats-portrait" src="https://github.com/user-attachments/assets/fee2b541-f097-4ee8-998c-302ddaae7b66" width="180" style="margin: 6px;"/>
  <img alt="academics-portrait" src="https://github.com/user-attachments/assets/7bda41fc-137d-49c7-937a-0d93778af514" width="180" style="margin: 6px;"/>
  <img alt="account-portrait" src="https://github.com/user-attachments/assets/b5cf73f9-decc-4e2f-b58b-f8481c335cc1" width="180" style="margin: 6px;"/>
  <img alt="profile-portrait" src="https://github.com/user-attachments/assets/63912860-6a72-4b16-9bc6-ab4623e61370" width="180" style="margin: 6px;"/>
</p>

<p align="center">
  <img alt="search-portrait" src="https://github.com/user-attachments/assets/42adf3a0-463c-470a-8d24-af524da4ca1c" width="180" style="margin: 6px;"/>
  <img alt="edit-course-portrait" src="https://github.com/user-attachments/assets/4aeff4e1-ef79-4929-8512-975be10ed67e" width="180" style="margin: 6px;"/>
  <img alt="year-details-portrait" src="https://github.com/user-attachments/assets/4bf04ecd-00de-4420-9ac7-c47ee01054e6" width="180" style="margin: 6px;"/>
  <img alt="semester_deets-portrait" src="https://github.com/user-attachments/assets/195664cc-2d36-44ac-9741-1fcc1926fd69" width="180" style="margin: 6px;"/>
</p>
