# Zenith '26 — Native Android Mobile App 🎄📱
### Christmas Wonderland & College Fest Management System

[![Android SDK](https://img.shields.io/badge/Android%20SDK-34-brightgreen.svg)](https://developer.android.com/)
[![Kotlin](https://img.shields.io/badge/Kotlin-1.9.22-purple.svg)](https://kotlinlang.org/)
[![Jetpack Compose](https://img.shields.io/badge/Jetpack%20Compose-BOM%202024.02.02-blue.svg)](https://developer.android.com/jetpack/compose)
[![Material 3](https://img.shields.io/badge/Material%203-1.2.0-orange.svg)](https://m3.material.io/)
[![Backend](https://img.shields.io/badge/Live%20Backend-Vercel%20FastAPI-black.svg)](https://hsb-fest-test-gamma.vercel.app/)

A high-performance, 100% native Android application built with **Kotlin** and **Jetpack Compose**, implementing a complete festival discovery, student registration, and administrative command system with an immersive **Christmas Wonderland experience**.

---

## 🌟 Key Features

### 🎓 1. Student Event Discovery & Christmas Experience
- **Christmas Wonderland Hero:** Deep Christmas crimson, pine green, ivory, and gold palette featuring festive script greetings and interactive holiday bells.
- **🎅 Animated Flying Santa Banner:** Santa in his sleigh pulled by Rudolph floating with realistic bobbing animations. Tap to catch gifts and trigger holiday celebration toasts.
- **⏳ Live Christmas Countdown Timer:** Real-time ticking countdown to December 25th at midnight in the device's local timezone.
- **🔍 Instant Search & Filter:** Real-time event search with 300ms debounce and 5 domain filters (*Technical, Cultural, Sports, Gaming, Workshop*).
- **🎟️ Real-Time Seat Capacity:** Instant visual status indicating seats remaining and sold-out states.
- **📝 Instant Registration Dialog:** Student registration modal with full input validation (name, roll number, college email).

### ⚡ 2. Admin Command Dashboard
- **📊 4 Core KPI Metrics:** Live computed cards for *Total Events*, *Total Registrations*, *Capacity Utilization %*, and *Upcoming Events*.
- **📈 Domain Category Distribution:** Real-time breakdown of event counts by category.
- **📋 Event Capacity & Demand Matrix:** Sorted descending by utilization %, highlighting high-demand events (>90% full) in warning red.
- **👥 Student Registrations Ledger:** Search and inspect every enrolled student with one-tap registration cancellation.
- **➕ Add New Event Modal:** Full CRUD capability to add events with client and server validation.
- **⚙️ Dynamic Server URL Configurator:** Easily switch the backend URL between:
  - **Vercel Cloud Production:** `https://hsb-fest-test-gamma.vercel.app/`
  - **Android Emulator:** `http://10.0.2.2:8081/`
  - **Localhost / Physical Device:** `http://<YOUR_IP>:8081/`

---

## 📦 Ready-to-Install APK

A pre-compiled, production-ready debug APK is included directly in this repository:
- **Download:** [`zenith26-app-debug.apk`](zenith26-app-debug.apk) (16 MB)
- **Default Cloud Endpoint:** `https://hsb-fest-test-gamma.vercel.app/` (No local server or setup needed!)

---

## 📲 Installation & Testing

### Option A: Web Browser Emulator (Appetize.io)
1. Visit [Appetize.io](https://appetize.io/upload).
2. Upload [`zenith26-app-debug.apk`](zenith26-app-debug.apk).
3. Test and interact with the app in your browser window.

### Option B: On an Android Device via ADB
```bash
adb install -r zenith26-app-debug.apk
```

### Option C: Direct Phone Install
1. Transfer `zenith26-app-debug.apk` to your Android device.
2. Tap the file in your file manager and select **Install** (enable "Install unknown apps" if prompted).

---

## 🛠️ Tech Stack & Architecture

| Layer | Technology |
|---|---|
| **Language** | Kotlin 1.9.22 |
| **UI Framework** | Jetpack Compose (BOM 2024.02.02) |
| **Design System** | Material 3 (`androidx.compose.material3`) |
| **Networking** | Retrofit 2.9.0 + OkHttp 4.12.0 |
| **JSON Serialization** | Gson (`converter-gson:2.9.0`) |
| **Async / Threading** | Kotlin Coroutines (`kotlinx-coroutines-android:1.7.3`) |
| **Architecture** | Single-Activity Architecture (`MainActivity.kt`) |
| **Backend API** | FastAPI + SQLite deployed on Vercel |

---

## 🏗️ Building from Source

### Prerequisites
- Android Studio Iguana / Jellyfish or newer
- JDK 17 (OpenJDK 17 recommended)
- Android SDK 34 (Build-Tools 34.0.0)

### Build Commands
```bash
# Clone the repository
git clone https://github.com/aabhaa750-alt/HSB_MobileAPP.git
cd HSB_MobileAPP

# Build Debug APK
./gradlew assembleDebug

# Output APK location:
# app/build/outputs/apk/debug/app-debug.apk
```

---

## 📂 Project Structure

```
HSB_MobileAPP/
├── app/
│   ├── build.gradle.kts
│   ├── proguard-rules.pro
│   └── src/main/
│       ├── AndroidManifest.xml
│       ├── java/com/zenith26/fest/
│       │   ├── MainActivity.kt
│       │   ├── ZenithApp.kt
│       │   ├── data/
│       │   │   ├── api/          # Retrofit API client & config
│       │   │   └── models/       # Event & Registration data models
│       │   └── ui/
│       │       ├── components/   # TopNavBar, Badges, ServerConfigDialog
│       │       ├── screens/
│       │       │   ├── student/  # HeroSection, Countdown, SantaBanner, EventCard
│       │       │   └── admin/    # StatsCards, EventMatrix, RegistrationsTable
│       │       └── theme/        # Color, Theme, Typography
│       └── res/                  # App icons, colors, themes, security config
├── gradle/wrapper/
├── build.gradle.kts
├── settings.gradle.kts
├── gradle.properties
├── gradlew & gradlew.bat
├── zenith26-app-debug.apk        # Pre-built release APK
└── README.md
```

---

## 📄 License
© 2026 Zenith College Fest Management System • Christmas Wonderland Edition
