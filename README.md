# 📊 Pocket Business Manager

**Pocket Business Manager** is a modern, India-focused mobile application built to help small business owners streamline their daily operations. With a premium UI and an offline-first architecture, it replaces the traditional bahi-khata with a smart, secure, and fast digital experience.

## ✨ Key Features

- **📒 Daily Hisaab (Transactions):** Easily record sales and expenses in under 10 seconds.
- **💳 Udhaar Tracking (Ledger):** Monitor credit given to and taken from customers with partial payment support and WhatsApp reminders.
- **📦 Inventory Control:** Track product stock levels (Stock In/Out) and get automatic low-stock alerts.
- **📊 Business Reports:** Generate Daily, Monthly, and Yearly reports with clear charts (Bar, Line, Pie). Export as PDF and share easily.
- **🧰 Built-in Smart Tools:** Quick access to a Calculator and a tailored GST Calculator.
- **🎨 Premium UI / UX:** Features a glassmorphic dark-first design with a unique curved bottom navigation bar. Fast performance with < 300ms load times.
- **🔄 Offline-First & Cloud Sync:** Works 100% offline. Automatically syncs data to Firebase when connected to the internet.

## 🛠️ Tech Stack

- **Frontend:** Flutter (Material 3)
- **State Management:** Riverpod
- **Local Database:** Isar (Source of Truth)
- **Backend & Cloud Database:** Firebase Auth (Google Sign-In), Cloud Firestore
- **Analytics & Monetization:** Firebase Analytics, Google AdMob
- **Architecture:** Clean Architecture

## 📱 App Structure

The app embraces an intuitive, 7-tab navigation system via a unique bottom wave bar:

1. 🏠 **Home:** At-a-glance dashboard with summary cards and quick actions.
2. 💸 **Transactions:** Filterable log of all business entries (Sale, Income, Expense, Purchase).
3. 📒 **Ledger:** Manage customer balances and Udhaar.
4. 📦 **Inventory:** Prevent stockouts with tracking and alerts.
5. 📊 **Reports:** Visual performance analysis and PDF export.
6. 🧰 **Tools:** Easy GST and standard calculations.
7. 👤 **Profile:** Settings, language, theme (Dark/Light/System), and sync management.

## 📸 App Screenshots

![sell screan](https://github.com/user-attachments/assets/a086ad4f-0a8c-42fc-9080-d190a4d283e8)
![new product screan](https://github.com/user-attachments/assets/f660417a-9c49-4934-bc03-d0cd7185619a)
![ledger screan](https://github.com/user-attachments/assets/628dd648-c7b3-42f2-982f-9bd9c7a22edb)
![home screan](https://github.com/user-attachments/assets/9db37a4c-4a56-4ef4-93a2-698659a6feab)
![add screan](https://github.com/user-attachments/assets/d5d4d63a-161e-4dc0-9596-6cd3435c3480)
![tools screan](https://github.com/user-attachments/assets/967fd890-e9ba-4e48-8453-0bfea6b86438)
![splash screan](https://github.com/user-attachments/assets/2d58d5ce-cb96-426d-95c2-38a868fbbc77)
![setting screan](https://github.com/user-attachments/assets/fe7c1c4f-02db-4356-a325-010b330572a9)




## 🚀 Getting Started

### Prerequisites
- Flutter SDK (`^3.x`)
- Dart SDK
- Firebase Project (configured with Firestore and Google Auth)

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/mdasifhusain6-art/pocket_business_manager.git
   ```
2. Navigate to the project directory:
   ```bash
   cd pocket_business_manager
   ```
3. Install dependencies:
   ```bash
   flutter pub get
   ```
4. Configure Firebase:
   Ensure you have the `google-services.json` (Android) and `GoogleService-Info.plist` (iOS) placed in their respective directories. You may use `flutterfire configure`.
5. Run the app:
   ```bash
   flutter run
   ```

## 🔒 Security & Privacy

- Full data ownership with secure Google OAuth 2.0 authentication.
- All data is primarily stored locally on the device via Isar.
- Secure, user-isolated cloud backup to Firestore (`allow read, write: if request.auth.uid == userId`).

## 🌐 Localization

- **English** (`en`)
- **Hindi** (`hi`)
- Number formats automatically adapt to the Indian system (e.g., ₹1,25,000).

---

*Pocket Business Manager — Your business, in your pocket.*

**Developed by MD ASIF HUSAIN**
