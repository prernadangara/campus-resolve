<div align="center">

  <img src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black" />
  <img src="https://img.shields.io/badge/Firestore-FFCA28?style=for-the-badge&logo=firebase&logoColor=black" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
  <img src="https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" />

  <h1>🏫 CampusResolve — Student Complaint Management System</h1>

  <p>
    A Firebase-powered web application for submitting, tracking and managing
    campus complaints through dedicated student and administrator portals.
  </p>

</div>

---

## Table of Contents

- [Overview](#overview)
- [System Architecture](#system-architecture)
- [Key Features](#key-features)
- [Technologies Used](#technologies-used)
- [How It Works](#how-it-works)
- [Security](#security)
- [Testing & Results](#testing--results)
- [Limitations](#limitations)
- [Future Scope](#future-scope)

---

## Overview

**CampusResolve** is a web-based complaint management system built using **JavaScript, Tailwind CSS, Firebase Authentication and Cloud Firestore**.

The system provides separate interfaces for students and administrators.

Students can submit campus-related complaints, optionally report them anonymously, track their status and view administrator resolutions.

Administrators can review complaints, filter them by category, assign priority, resolve issues and broadcast campus-wide announcements.

The project demonstrates practical implementation of **authentication, cloud databases, real-time updates and database-level access control**.

---

## System Architecture

    ┌──────────────┐
    │   Student    │
    └──────┬───────┘
           │
           ▼
    ┌──────────────────┐
    │  Student Portal  │
    │                  │
    │ Authentication   │
    │ Complaints       │
    │ Anonymous Report │
    │ Tracking         │
    └────────┬─────────┘
             │
             ▼
    ┌──────────────────┐
    │ Firebase Auth    │
    │       +          │
    │ Cloud Firestore  │
    └────────┬─────────┘
             │
             ▼
    ┌──────────────────┐
    │   Admin Portal   │
    │                  │
    │ Review           │
    │ Filter           │
    │ Prioritize       │
    │ Resolve          │
    │ Broadcast        │
    └──────────────────┘

---

## Key Features

### 👨‍🎓 Student Portal

- Email/password authentication
- Complaint submission with categories
- Anonymous complaint option
- Personal complaint tracking
- Pending and resolved status
- Administrator resolution notes
- Real-time campus announcement ticker
- Empty-state handling
- Toast notifications

### 🛠️ Admin Portal

- Dedicated administrator authentication
- Complaint statistics dashboard
- Category-based filtering
- Normal / urgent priority management
- Complaint resolution with closing remarks
- Complaint deletion
- Campus-wide announcement broadcasting
- Empty-state handling
- Toast notifications

### 🔒 Anonymous Reporting

Anonymous complaints hide the student's email and generated ID from the administrator while retaining the authenticated Firebase UID internally.

This allows the student to remain anonymous to the administrator while still tracking their own complaint.

---

## Technologies Used

| Technology | Purpose |
|---|---|
| **HTML5** | Application structure |
| **JavaScript** | Application logic |
| **Tailwind CSS** | Responsive UI styling |
| **Firebase Authentication** | User authentication |
| **Cloud Firestore** | Complaint & announcement storage |
| **Firebase SDK** | Firebase integration |
| **Firestore onSnapshot** | Real-time updates |

---

## How It Works

### Student Complaint Flow

    Student
       ↓
    Login / Create Account
       ↓
    Submit Complaint
       ↓
    Cloud Firestore
       ↓
    Admin Reviews
       ↓
    Resolve + Add Remark
       ↓
    Student Tracking History

### Announcement Flow

    Admin
       ↓
    Broadcast Announcement
       ↓
    Cloud Firestore
       ↓
    Student Portal
       ↓
    Moving Campus News Ticker

---

## Security

CampusResolve uses **Firebase Authentication and Cloud Firestore Security Rules** for database access control.

The implemented security model allows:

- Students to create complaints associated with their own UID.
- Students to read only their own complaints.
- Students to read campus announcements.
- Students to modify or delete neither complaints nor announcements.
- The administrator to view and manage all complaints.
- Only the administrator to update or delete complaints.
- Only the administrator to create, update or delete announcements.
- Unauthenticated users to be denied Firestore access.

Database-level rules are used rather than relying only on frontend restrictions.

---

## Testing & Results

The application was tested using separate student and administrator accounts.

| Test | Result |
|---|---|
| Student account creation | ✅ Passed |
| Student authentication | ✅ Passed |
| Complaint submission | ✅ Passed |
| Anonymous complaint | ✅ Passed |
| Personal complaint tracking | ✅ Passed |
| Admin authentication | ✅ Passed |
| Complaint filtering | ✅ Passed |
| Priority management | ✅ Passed |
| Complaint resolution | ✅ Passed |
| Resolution notes | ✅ Passed |
| Announcement broadcasting | ✅ Passed |
| Moving announcement ticker | ✅ Passed |
| Empty-state handling | ✅ Passed |
| Firestore security rules | ✅ Passed |

---

## Limitations

- Currently designed around a single administrator account.
- Uses predefined complaint categories.
- No file attachments for complaints.
- Requires an active internet connection for Firebase services.
- Currently implemented as a lightweight frontend application.

---

## Future Scope

- Complaint analytics and reporting
- Advanced search and filtering
- File attachments
- Email or push notifications
- Multiple administrator roles
- Additional complaint categories
- Production deployment
- Enhanced accessibility

---

## Project Information

**Project:** CampusResolve  
**Type:** Student Complaint Management System  
**Platform:** Firebase  
**Focus Areas:** Web Development, Firebase, Authentication, Cloud Database, Real-Time Applications

---

<div align="center">

### 🏫 CampusResolve

**Report • Track • Resolve**

</div>
