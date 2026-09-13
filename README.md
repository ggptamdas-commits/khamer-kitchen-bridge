# Khamer Kitchen Bridge (مطعم خامر) & Multi-Restaurant SaaS

**Real-Time Kitchen ↔ Cashier Communication & Customer QR Digital Menu Platform**  
**منصة التواصل الفوري بين المطبخ والكاشير وقائمة الزبائن الرقمية المباشرة**

A lightweight, production-ready, zero-build single-page web application designed for real-time restaurant operations: instant status bridging between kitchen and cashier, self-service restaurant administration, and live customer digital QR menu.

---

## 🌟 Key Features

- **Strictly Operational & Communication-Focused**: No ordering, checkout, or POS fiscal clutter. Completely compliant and friction-free.
- **Instant Real-Time Sync**: Powered by Firebase Firestore `onSnapshot()` listeners for sub-second updates.
- **Four Specialized Stations / Views**:
  - 🏢 **Admin / Owner Dashboard**:
    - **Restaurant Identity**: Customize Restaurant Name (Arabic & English), Slogan / Tagline, and Logo.
    - **Staff Accounts & PINs**: Configure 4-digit quick-access PINs for Kitchen and Cashier with 1-click direct link copy.
    - **Food Item Management**: Add new items (with Arabic/English names, category, price in SAR, prep time, and image URL) and delete items in real time.
    - **Table QR Code Generator**: Generate and print table QR codes for customer digital menus.
  - 👨‍🍳 **Kitchen Station**: Touch-friendly availability toggles (Available, Out of Stock, Delayed, Low Stock), delay timers (+5m, +10m, +15m), kitchen workload status, and emergency alert broadcast.
  - 💵 **Cashier Station**: Live overview of unavailable and delayed items with countdowns, available-again alerts, search, category filters, and audio chime notifications.
  - 📱 **Customer Digital QR Menu (`?station=customer`)**: Fast, mobile-first live menu view showing real-time availability badges (🟢 متوفر / 🔴 غير متوفر / ⏳ تأخير مؤقت), category filters, and search.
- **Direct Station URLs & Access**:
  - Customer Menu: `/?station=customer`
  - Kitchen Tablet: `/?station=kitchen&pin=4433`
  - Cashier Station: `/?station=cashier&pin=1122`
  - Admin Dashboard: `/?station=admin`
  - Multi-Tenant Support: `/?r=restaurant_slug` (scopes data per restaurant)
- **Audio & Visual Alert Engine**: Multi-priority Web Audio chime synthesizer (Low, Normal, High, Critical) with zero external asset dependencies.
- **Bilingual & Themes**: Full Arabic (RTL) and English (LTR) localization with Light & Dark mode support.

---

## 🚀 Setup & Deployment Guide

### 1. Firebase Setup
1. Go to the [Firebase Console](https://console.firebase.google.com/) and create a project (e.g. `khamer-kitchen` in Region `me-central2` Dammam).
2. Enable **Firestore Database** and set rules from `firestore.rules`.
3. Add your Firebase Web App config in `index.html`.

### 2. Deploying to Vercel
1. Connect this repository to [Vercel](https://vercel.com).
2. Framework Preset: **Other** (Static HTML).
3. Click **Deploy** for instantaneous global CDN deployment.

---

Developed for **Khamer Restaurant (مطعم خامر)** & Local Cafes in Saudi Arabia.
