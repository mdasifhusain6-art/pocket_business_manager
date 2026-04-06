# 📋 Product Requirements Document (PRD)

## Pocket Business Manager – Premium UI Edition

| Field | Detail |
|---|---|
| **Version** | 1.1.0 |
| **Status** | Draft |
| **Platform** | Flutter (Android & iOS) |
| **Target Market** | India – Small Business Owners |
| **Currency** | ₹ INR (Format: ₹1,25,000) |

---

## 1. 🎯 Product Goal

**Pocket Business Manager** is a modern, India-focused mobile application built to help small business owners with:

| Goal | Description |
|---|---|
| 📒 Daily Hisaab | Record sales and expenses quickly, every day |
| 💳 Udhaar Tracking | Monitor credit given to and taken from customers |
| 📦 Inventory Control | Track product stock levels and get low-stock alerts |
| 📊 Report Generation | Visualize business performance and export PDF reports |

### Core Focus
- ✅ **Simple UI** — No clutter, no learning curve
- ✅ **Fast Performance** — Every screen loads in < 300ms
- ✅ **Offline-First** — Works fully without internet; syncs when online

The app is built with an **offline-first architecture**: data is stored locally using **Isar** and securely synced and backed up via **Firebase**. It features a unique curved bottom navigation bar, a glassmorphic dark-first premium UI, and smart built-in tools (Calculator, GST Calculator) to accelerate daily business operations.

---

## 2. 🧭 Goals & Success Metrics

### Primary Goals
- Enable small business owners to record sales and expenses in under 10 seconds.
- Provide clear daily/monthly profit visibility without any accounting knowledge.
- Offer a reliable offline-first experience with seamless cloud sync.

### Success Metrics
| Metric | Target |
|---|---|
| Daily Active Users (DAU) | 5,000+ within 6 months |
| Session Length | ≥ 4 minutes average |
| Crash-Free Rate | ≥ 99.5% |
| Sync Success Rate | ≥ 98% |
| AdMob Revenue | ₹20,000–₹50,000/month |

---

## 3. 👤 Target Users

| Persona | Description |
|---|---|
| **Kirana Store Owner** | Tracks daily sales, credit given to customers, and stock. |
| **Small Trader / Wholesaler** | Needs GST calculations and monthly profit reports. |
| **Service Provider** | Manages outstanding payments (Udhaar) and invoices. |
| **Home Business Owner** | Tracks income/expense with simple, clean UI. |

**Common Traits:**
- Prefer Hindi or English UI
- Use Android smartphones (primary)
- Limited accounting knowledge
- Need fast, intuitive data entry

---

## 4. 🎨 UI / Design System

### 4.1 Design Language
| Property | Value |
|---|---|
| Style | Minimalist + Clean |
| Card Style | Glassmorphism |
| Button Style | Soft Neumorphism |
| Theme Default | Dark-first |
| Highlights | Neon accent |

### 4.2 Color Palette
| Role | Color |
|---|---|
| Background (primary) | `#0F172A` |
| Background (deep) | `#020617` |
| Primary | Deep Blue |
| Accent | Neon Blue / Cyan |
| Income / Profit | Green |
| Expense / Loss | Red |
| Text (primary) | White |
| Text (secondary) | Gray |

### 4.3 Typography
- Font: **Inter** or **Poppins**
- Use clear hierarchy: Heading → Subheading → Body → Caption

### 4.4 Design Rules
- ❌ No UI clutter
- ❌ No forced login on first open
- ❌ No excessive animations
- ✅ Every screen must load in < 300ms (local data)
- ✅ All monetary values formatted as ₹X,XX,XXX

---

## 5. 📱 Navigation System

### 5.1 Bottom Navigation Bar (Unique Design)
| Property | Detail |
|---|---|
| Shape | Curved / Wave bottom bar |
| Center Element | Floating FAB ("+") with notch |
| Active State | Icon pop-up with label |
| Animation | Smooth transition (≤ 200ms) |

### 5.2 Navigation Tabs
| # | Tab | Icon | Description |
|---|---|---|---|
| 1 | Home | 🏠 | Dashboard & summary |
| 2 | Transactions | 💸 | All entries |
| 3 | Ledger | 📒 | Udhaar / credit tracking |
| 4 | Inventory | 📦 | Stock management |
| 5 | Reports | 📊 | Charts & analysis |
| 6 | Tools | 🧰 | Calculator, GST tool |
| 7 | Profile | 👤 | Settings & account |

### 5.3 FAB (Floating Action Button)
- **Center "+" button** in the navigation notch
- Opens a **Quick Entry Bottom Sheet** with options:
  - ➕ Add Sale
  - ➖ Add Expense
  - 📒 Add Udhaar
  - 📦 Add Stock

---

## 6. 🏠 Feature: Home (Dashboard)

### Purpose
Give the user an instant snapshot of their business health at a glance.

### UI Sections

#### 6.1 Summary Cards (Top Row)
| Card | Value Shown | Color Indicator |
|---|---|---|
| Sales | Total sales (today/this month) | Blue |
| Expense | Total expenses | Red |
| Profit | Net profit (Sales - Expense) | Green |
| Cash | Current cash balance | Cyan |

- Each card uses glassmorphism style
- Tappable → navigates to detailed breakdown

#### 6.2 Recent Transactions (List)
- Show last 5–10 transactions
- Income entries → Green left border
- Expense entries → Red left border
- Each row: Category icon | Title | Amount | Time

#### 6.3 Quick Actions (Grid)
| Action | Icon |
|---|---|
| Add Sale | 💰 |
| Add Expense | 🧾 |
| Add Udhaar | 📒 |
| Add Stock | 📦 |

---

## 7. 💸 Feature: Transactions

### Purpose
A complete, searchable, and filterable log of all business entries.

### Entry Types
| Type | Description | Color |
|---|---|---|
| Sale | Revenue from selling products/services | 🟢 Green |
| Income | Other income (interest, refunds, etc.) | 🟢 Green |
| Expense | Business operating costs | 🔴 Red |
| Purchase | Stock/inventory buying costs | 🔴 Red |

### Requirements
| Requirement | Detail |
|---|---|
| View all entries | Paginated list, newest first |
| Filter by date | Today / This Week / This Month / Custom Range |
| Filter by type | Sale / Income / Expense / Purchase / All |
| Search | By name, category, note |
| Entry actions | Edit ✏️ / Delete 🗑️ (with confirmation) |
| Entry fields | Date, Type, Category, Amount (₹), Note, Payment mode |

### Entry Categories
- **Income:** Sale, Service, Other Income
- **Expense:** Purchase, Rent, Salary, Transport, Utility, Other

---

## 8. 📒 Feature: Ledger (Udhaar)

### Purpose
Track credit given to or taken from customers/suppliers.

### Requirements
| Requirement | Detail |
|---|---|
| Customer list | Name, Phone, Net balance (Debit/Credit) |
| Add customer | Name, Phone (optional) |
| Customer detail | Full transaction history |
| Add entry | Credit (they owe you) / Debit (you paid them back) |
| Partial payment | Record partial repayments; balance auto-updates |
| Balance color | Green (they owe you) / Red (you owe them) |
| Search | By customer name |
| WhatsApp reminder | Share balance summary via WhatsApp |

---

## 9. 📦 Feature: Inventory Management

### Purpose
Help business owners track product stock levels to avoid running out or overstocking.

### Requirements
| Requirement | Detail |
|---|---|
| Add product | Name, Price (₹), Unit (kg/pcs/litre), Opening stock |
| Stock In | Record stock received (purchase/restocking) |
| Stock Out | Record stock used or sold |
| Current quantity | Always up-to-date after each in/out entry |
| Low stock alert | Badge/notification when quantity falls below threshold |
| Product list | Sorted by low stock first, searchable |
| Stock report | Per-product stock history and movement summary |

### Low Stock Alert Rules
- User sets threshold per product (default: 5 units)
- Alert shown as a badge on the Inventory tab icon
- Dashboard also shows a "Low Stock" warning card when triggered

---

## 10. 📊 Feature: Reports

### Purpose
Visual and exportable business performance analysis.

### Report Types
| Report | Description |
|---|---|
| Daily Report | Transactions for a selected day |
| Monthly Report | Month-wise P&L summary |
| Yearly Report | Year-over-year comparison |
| Profit Analysis | Revenue vs Expense chart |
| Expense Breakdown | Pie chart by expense category |
| Stock Report | Per-product stock movement and current levels |

### Chart Types
- Bar Chart (monthly comparison)
- Line Chart (trend over time)
- Pie Chart (expense breakdown by category)

### Export & Share
| Feature | Detail |
|---|---|
| PDF Export | Full report with business name, date range, charts, table |
| Share | Share PDF via WhatsApp, Gmail, or any app |
| PDF includes | Business name, logo (if set), date range, summary, charts |

---

## 11. 🧰 Feature: Tools

### 11.1 Basic Calculator
| Property | Detail |
|---|---|
| Operations | +, −, ×, ÷, %, C, ± |
| Design | Large buttons, dark theme, numpad layout |
| History | Last 5 calculations shown |

### 11.2 GST Calculator
| Property | Detail |
|---|---|
| Modes | Add GST / Remove GST |
| GST Rates | 5%, 12%, 18%, 28% |
| Input | Base amount (₹) |
| Output | GST amount + Total amount |
| Display | Breakdown: Base + GST = Total |

---

## 12. 👤 Feature: Profile & Settings

### Sections

#### 12.1 Profile
| Field | Detail |
|---|---|
| User Name | From Google Auth |
| Email | From Google Auth |
| Profile Photo | From Google or custom |
| Business Name | User-configured |
| Business Type | Dropdown (Retail, Service, etc.) |
| Phone Number | Optional |

#### 12.2 History
- Recent app activity log (last 20 actions)

#### 12.3 Theme
| Option | Value |
|---|---|
| System Default | Follows device theme |
| Light Mode | Light background |
| Dark Mode | `#0F172A` background (default) |

#### 12.4 Language
- Hindi 🇮🇳
- English 🇬🇧

#### 12.5 Backup & Sync
| Item | Detail |
|---|---|
| Sync Status | Last synced timestamp |
| Manual Sync | "Sync Now" button |
| Auto-sync | On app open + every 15 min (if online) |

#### 12.6 Legal
- Privacy Policy
- Terms & Conditions
- About Us (Version info)

#### 12.7 Logout
- Confirmation dialog before logout
- Local data retained after logout

---

## 13. 🏗️ Technical Architecture

### 13.1 Tech Stack
| Layer | Technology |
|---|---|
| **Frontend** | Flutter (Material 3) |
| **State Management** | Riverpod |
| **Local Database** | Isar |
| **Authentication** | Firebase Auth (Google Sign-In) |
| **Cloud Database** | Cloud Firestore |
| **Analytics** | Firebase Analytics |
| **Ads** | AdMob |

### 13.2 Project Structure
```
lib/
├── presentation/         # UI screens, widgets, themes
│   ├── home/
│   ├── transactions/
│   ├── ledger/
│   ├── inventory/
│   ├── reports/
│   ├── tools/
│   └── profile/
├── domain/               # Business logic, models, use cases
│   ├── models/
│   └── usecases/
├── data/                 # Repositories, local DB, remote API
│   ├── local/            # Isar collections
│   └── remote/           # Firestore services
└── core/                 # Constants, utils, themes, DI
    ├── theme/
    ├── constants/
    └── di/
```

### 13.3 Local Database Schema (Isar)

#### Transaction
```dart
@collection
class Transaction {
  Id id = Isar.autoIncrement;
  late String title;
  late double amount;
  late String type;          // 'sale' | 'income' | 'expense' | 'purchase'
  late String category;
  late String paymentMode;
  String? note;
  late DateTime date;
  late DateTime createdAt;
  late DateTime updatedAt;
  bool isSynced = false;
  String? firebaseId;
}
```

#### Customer (Ledger)
```dart
@collection
class Customer {
  Id id = Isar.autoIncrement;
  late String name;
  String? phone;
  double balance = 0.0;      // positive = they owe you
  late DateTime createdAt;
  late DateTime updatedAt;
  bool isSynced = false;
  String? firebaseId;
}
```

#### Product (Inventory)
```dart
@collection
class Product {
  Id id = Isar.autoIncrement;
  late String name;
  late double price;
  int stock = 0;
  String? unit;
  int lowStockThreshold = 5; // alert when stock <= this value
  late DateTime updatedAt;
  bool isSynced = false;
  String? firebaseId;
}
```

#### Business
```dart
@collection
class Business {
  Id id = Isar.autoIncrement;
  late String name;
  late String type;
  String? phone;
  String? address;
  String? gstin;
  late DateTime updatedAt;
}
```

### 13.4 Cloud Database Schema (Firestore)
```
users/
  {userId}/
    profile: { name, email, photoUrl, businessName, ... }
    businesses/
      {businessId}/
        transactions/
          {transactionId}: { ...Transaction fields }
        customers/
          {customerId}: { ...Customer fields }
        products/
          {productId}: { ...Product fields }
```

---

## 14. 🔄 Data Flow (Offline-First)

### 14.1 Flow by Login State

| State | Behaviour |
|---|---|
| **Without Login** | All data stored locally in Isar only |
| **After Login** | Local data synced to Firebase; new devices can restore |
| **New Device** | Login → full data restored from Firestore to Isar |

### 14.2 Sync Logic
```
User Action
    ↓
Save to Isar (Local) → isSynced = false
    ↓
Check Internet Connection
    ↓ (if online)
Push to Firestore → isSynced = true, firebaseId = docId
    ↓
On App Open / Manual Sync
    ↓
Fetch Firestore changes (updatedAt > lastSyncTime)
    ↓
Merge with Local (Latest updatedAt wins)
```

### 14.3 Sync Rules
| Rule | Detail |
|---|---|
| Conflict resolution | Latest `updatedAt` timestamp wins |
| Offline support | All operations work fully offline |
| Sync trigger | App open + network reconnect + manual |
| Sync indicator | Subtle icon in app bar showing sync status |
| `isSynced` flag | Every Isar record carries this boolean |
| `updatedAt` field | Every record updated on every write |

---

## 15. 💰 Monetization Strategy

| Channel | Detail |
|---|---|
| **AdMob Banner Ads** | Shown on Reports and Tools screens |
| **AdMob Interstitial** | Shown after every 5th transaction entry |
| **AdMob Rewarded** | Unlock extra report features (optional) |
| **Estimated Revenue** | ₹20,000 – ₹50,000/month at scale |

### Ad Placement Rules
- ❌ No ads on Home or data-entry screens
- ❌ No ads that block core workflows
- ✅ Ads only on report views and tools (non-critical screens)

---

## 16. 🚀 Development Roadmap

### Phase 1 – Foundation (Weeks 1–3)
- [ ] Project setup (Flutter + Riverpod + Isar)
- [ ] Theme system (Dark mode, colors, typography)
- [ ] Custom bottom navigation bar
- [ ] Home Dashboard UI
- [ ] Add/Edit/Delete Transactions (Sale, Income, Expense, Purchase)
- [ ] Local storage (Isar)

### Phase 2 – Core Features (Weeks 4–6)
- [ ] Ledger (Udhaar) module with partial payment
- [ ] Customer management
- [ ] Inventory management (Stock In/Out, low stock alert)
- [ ] Calculator tool
- [ ] GST Calculator tool

### Phase 3 – Reports & Profile (Weeks 7–8)
- [ ] Daily / Monthly / Yearly reports
- [ ] Stock report
- [ ] Charts integration (fl_chart)
- [ ] PDF export + share functionality
- [ ] Profile & Settings screen
- [ ] Language switching (Hindi/English)
- [ ] Theme switching (System / Light / Dark)

### Phase 4 – Firebase Integration (Weeks 9–12)
- [ ] Firebase Auth (Google Sign-In)
- [ ] Firestore integration
- [ ] Sync engine implementation
- [ ] Data restore on new device
- [ ] AdMob integration
- [ ] Testing (unit + widget + integration)
- [ ] Performance optimization
- [ ] Play Store release

---

## 17. ⚠️ Important Rules & Constraints

| Rule | Description |
|---|---|
| ❌ No forced login | App must work fully offline without sign-in |
| ❌ No UI clutter | Every screen must feel clean and minimal |
| ❌ No skipped sync | All local changes must eventually sync |
| ❌ No heavy animations | Transitions ≤ 200ms; no particle effects |
| ✅ Offline-first | Local Isar DB is the source of truth |
| ✅ Fast entry | Adding a transaction must take < 10 seconds |
| ✅ Data safety | No data loss on app crash or force close |
| ✅ INR only | All monetary display uses ₹ with Indian formatting |

---

## 18. 🔐 Security & Privacy

| Area | Requirement |
|---|---|
| Authentication | Firebase Auth (Google OAuth 2.0) |
| Data at rest | Isar local DB (device storage) |
| Data in transit | HTTPS (Firestore default) |
| User data | Each user only accesses their own Firestore path |
| Firestore rules | `allow read, write: if request.auth.uid == userId` |
| No sensitive ads | AdMob configured for family-safe, business categories |

---

## 19. 🌐 Localization

| Language | Code | Status |
|---|---|---|
| English | `en` | ✅ Primary |
| Hindi | `hi` | ✅ Required |

- All strings must be externalized in ARB files
- Number formatting: Indian system (1,00,000 not 100,000)
- Date formatting: DD/MM/YYYY

---

## 20. 📦 Key Dependencies (Flutter)

```yaml
dependencies:
  flutter_riverpod: ^2.x
  isar: ^3.x
  isar_flutter_libs: ^3.x
  firebase_core: ^2.x
  firebase_auth: ^4.x
  cloud_firestore: ^4.x
  google_sign_in: ^6.x
  fl_chart: ^0.x
  pdf: ^3.x
  printing: ^5.x
  google_mobile_ads: ^3.x
  intl: ^0.x
  shared_preferences: ^2.x
  connectivity_plus: ^4.x
  path_provider: ^2.x
```

---

## 21. 🎯 Final Vision

> **Pocket Business Manager** will be the go-to app for India's 60+ million small business owners — a fast, beautiful, and reliable tool that fits in their pocket and replaces the traditional bahi-khata with a smart, modern experience.

**The app delivers:**
- 🔥 Premium UI + Unique Curved Navigation
- 🔥 Complete Business Management (Transactions + Ledger + Inventory)
- 🔥 Smart Built-in Tools (Calculator + GST)
- 🔥 Offline-First + Firebase Sync & Restore
- 🔥 Scalable, Clean Architecture — Production Ready

---

*Document maintained by the Product & Engineering team. Version 1.1.0 — Last updated: March 2026.*