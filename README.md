# Khamer Kitchen Bridge (مطعم خامر)

**Real-Time Kitchen ↔ Cashier Communication System**  
**نظام التواصل الفوري بين المطبخ والكاشير**

A lightweight, production-ready, zero-build single-page web application designed exclusively for instant communication between the kitchen and cashier staff at Khamer Restaurant.

---

## 🌟 Key Features

- **Strictly Communication-Focused**: No ordering, checkout, or POS clutter. 100% optimized for kitchen-cashier coordination.
- **Instant Real-Time Sync**: Powered by Firebase Firestore `onSnapshot()` listeners for sub-second updates.
- **Three Specialized Dashboards**:
  - 👨‍🍳 **Kitchen**: Touch-friendly status changes (Available, Out of Stock, Delayed, Low Stock), delay timers (+5m, +10m, +15m), kitchen workload status, and emergency alert broadcast.
  - 💵 **Cashier**: Live overview of unavailable and delayed items with countdowns, available-again alerts, search, category filters, and fast messaging.
  - 👑 **Admin**: Menu item management, sample data seeder, notification audit logs, and test broadcast tools.
- **🖥️ Cashier Always-On Display Mode**: Full-screen TV/desktop view with large digital clock, live status counters, and alerts.
- **Audio & Visual Alert Engine**: Multi-priority Web Audio chime synthesizer (Low, Normal, High, Critical) with zero external asset dependencies.
- **Bilingual & Themes**: Full Arabic (RTL) and English (LTR) localization with Light & Dark mode support.

---

## 🚀 Setup & Deployment Guide

### 1. Firebase Setup
1. Go to the [Firebase Console](https://console.firebase.google.com/) and create a new project named `khamer-kitchen`.
2. Navigate to **Authentication** > **Sign-in method** and enable **Email/Password**.
3. Navigate to **Firestore Database** > **Create database** (Start in Test Mode or Production Mode).
4. In Firestore **Rules**, paste the contents of `firestore.rules`.
5. Go to **Project Settings** > **General** > **Your apps** > Add a **Web app** (`</>`).
6. Copy the `firebaseConfig` object and paste it into `index.html`:
   ```javascript
   const firebaseConfig = {
     apiKey: "YOUR_API_KEY",
     authDomain: "YOUR_PROJECT.firebaseapp.com",
     projectId: "YOUR_PROJECT",
     storageBucket: "YOUR_PROJECT.appspot.com",
     messagingSenderId: "...",
     appId: "..."
   };
   ```

### 2. Deploying to Vercel
1. Import this repository into [Vercel](https://vercel.com).
2. Framework Preset: **Other** (Static HTML).
3. Click **Deploy**. Vercel will immediately host `index.html` on a fast CDN!

### 3. Deploying to GitHub Pages
1. Go to **Settings** > **Pages** in this GitHub repository.
2. Under **Branch**, select `main` and `/ (root)`, then click **Save**.

---

## 👥 Demo Logins / User Setup

You can test the app immediately using the built-in **Quick Preview Mode** buttons or create Firebase Auth accounts:
- **Kitchen Staff**: `kitchen@khamer.com`
- **Cashier**: `cashier@khamer.com`
- **Admin**: `admin@khamer.com`

---

Developed for **Khamer Restaurant (مطعم خامر)**.
