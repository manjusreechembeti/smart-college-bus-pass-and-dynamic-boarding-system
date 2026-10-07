# Smart College Bus Pass & Dynamic Boarding System
> **Safe Rides • Smart Verification • Better Campus**  
> *Your Pass • Your Ride • Our Priority*

A high-performance, client-side college transit management platform implementing real-time QR credentialing, role-based access control, dynamic temporary boarding permits, fee enforcement, and automated driver gate verification.

---

## 🎨 Theme & Design System

- **Primary Brand Theme**: **Forest Emerald & Mint Green** (`#059669`, `#10b981`) paired with **Sunset Amber & Warm Topaz** (`#f59e0b`, `#d97706`).
- **Strict Color Policy**: 100% free of blue, violet, indigo, or purple hues.
- **Dual Theme Support**: Full **Light Mode** & **Dark Mode** toggle available via the top-right button on the Login screen, the top Navbar, and the Sidebar.
- **Initial Landing Experience**: **Login Page appears directly** on first visit and fresh page loads.

---

## 📸 Modules & Features

1. **Gate Terminal AP-39 (Login & Sign Up)**: Direct landing view featuring:
   - **Gate Sign In**: 1-Tap RFID passkey scan (with Web Audio chime & confetti) or manual Roll No/PIN entry for Student, Driver, and Admin roles.
   - **Student Bus Pass Sign Up**: Comprehensive registration portal for new students (Full Name, Roll No, Branch, Academic Year, Class Section, College Email, Phone Number, Requested Route, Pickup Stop, 4-digit PIN, and Photo Badge selection) that updates the 3D Holographic Card preview in real-time.
   - **Interactive 3D Holographic Pass**: Realistic metallic EMV chip, NFC wave telemetry, scanning laser beam, and dynamic student photo.
2. **Collapsible Navigation Sidebar**:
   - Compact collapsible state displaying **only icons** (`w-20`) or expanded state with **icons & labels** (`w-64`).
   - Houses core navigation: **Dashboard**, **College Bus Pass**, **Request Other Bus**, **Boarding**, and **Receipts**.
   - Expand/collapse menu button located both at the top of the sidebar and inside the top Navbar.
3. **Top Navbar with Three-Dot (⋮) Menu & Stepper**:
   - **Three-Dot (⋮) Menu**: Glassmorphic dropdown menu providing 1-click access to **Dashboard** and all available pages.
   - **Single Horizontal Line Stepper**: Replaced separate boxes with a continuous clickable horizontal line for guided student experience journey.
4. **Student Dashboard**: 4 key indicator tiles (*Fee Status [Paid]*, *Regular Bus [Route - 3]*, *Pass Validity [2025-2026 Valid]*, *Temporary Access [1 Pending]*), scannable dynamic QR pass card, recent activity ledger, and temporary bus request prompt.
5. **Bus Pass Details**: Official printable digital transportation identity card with scannable QR payload, branch metadata, validity, and boarding audit trail.
6. **Temporary Bus Request**: Interactive multi-field request workflow (date selection, alternate route picker, purpose selection, additional justification) with a vertical 4-stage live status tracker (*Requested → Under Review → Approved / Rejected*).
7. **Driver Terminal (Verification)**: Mobile-optimized conductor terminal with real-time QR & Roll Number search, audio chime/buzz feedback (Web Audio API), confetti celebration, dynamic boarding list, and 1-click confirmation.
8. **Admin Dashboard**: Comprehensive transit control console with global statistics (*1,248 Total Students, 1,102 Paid, 146 Unpaid*), circular 88% fee collection donut gauge, real-time temporary request approval/rejection queue, and college-wide boarding records.
9. **Verification Result Engine**:
   - 🟢 **Allowed (Fee Paid - Regular Bus)**: *Priya Sharma (22CSQ01) → Boarding Allowed (Emerald)*
   - 🟡 **Temporary Access (Approved - Alternate Bus)**: *Sneha Reddy (22CSQ32) → Boarding Allowed (Amber)*
   - 🔴 **Not Allowed (Fee Not Paid)**: *Rahul Kumar (22CSQ45) → Boarding Denied (Rose)*

---

## 📂 Project Structure

```text
smart-bus-pass/
│
├── frontend/
│   │
│   ├── public/
│   │   ├── images/
│   │   ├── icons/
│   │   └── favicon.ico
│   │
│   ├── src/
│   │   ├── assets/
│   │   ├── components/
│   │   ├── context/
│   │   └── data/
│   │
│   ├── package.json
│   ├── vite.config.js
│   ├── eslint.config.js
│   └── .env.example
│
├── backend/
│   └──          ← empty for now
│
├── docs/
│   └──           ← can be added later
│
├── .gitignore
└── README.md
```

---

## 🚀 Quick Start Guide

### 1. Navigate to Frontend & Install Dependencies
```bash
cd frontend
npm install
```

### 2. Start Development Server
```bash
npm run dev
```
Open [http://localhost:5173](http://localhost:5173) in your browser. The **Login Page** will open directly.

### 3. Build for Production
```bash
npm run build
```

---

## 🔑 Demo Personas & Credentials

| Role | Name | Roll / Email | Default State |
|---|---|---|---|
| **Student (Regular)** | Priya Sharma | `22CSQ01` | Fee Paid • Assigned Route 3 |
| **Student (Temp Pass)** | Sneha Reddy | `22CSQ32` | Fee Paid • Approved Temp Pass for Route 5 |
| **Student (Unpaid)** | Rahul Kumar | `22CSQ45` | Fee Unpaid • Pass Suspended |
| **Driver** | Ramesh Kumar | `AP 39 TS 1234` | Conductor for Route - 3 |
| **Admin** | Transport In-Charge | `admin` | Full Approval & Fleet Authority |
