# LOFO - Lost It? Found It. Prove It. 🔍

[![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)](https://nodejs.org/)
[![MySQL](https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/)
[![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)](https://github.com/)

> **"Lost It? Found It. Prove It."** - A secure, proof-based lost and found management system.

---

## 📌 Overview

LOFO is a full-stack solution designed to streamline the process of reporting and retrieving lost items. Unlike traditional systems, LOFO implements a **Proof-Based Verification System**, ensuring that items are returned only after valid evidence (like photos or receipts) has been reviewed and approved by administrators.

This reduces fraudulent claims and builds a community of trust.

---

## ✨ Features

- **🔍 Item Discovery**: Easily search and filter through reported items.
- **📝 Report Lost/Found Items**: Structured forms to log items with descriptions and locations.
- **📦 Claim System**: Seamlessly initiate a claim for any lost item.
- **🔐 Proof-Based Verification**: Securely upload evidence artifacts to prove ownership.
- **🛠️ Admin Approval System**: Dedicated dashboard for admins to adjudicate claims.
- **📊 Dashboard & Analytics**: Visualized metrics for active, pending, and resolved cases.

---

## 🏗️ Tech Stack

### Frontend
- **React** (Vite)
- **Tailwind CSS** (Styling)
- **Zustand** (State Management)

### Backend
- **Node.js**
- **Express**
- **JWT** (Authentication)
- **Multer** (File Uploads)

### Database
- **MySQL** (Normalized schema with Triggers and Stored Procedures)

---

## 📂 Project Structure

```text
lofofinal/
├── lofo-app/           # Frontend (React + Vite)
│   ├── src/            # Application logic
├── server/             # Backend (Node.js + Express)
│   ├── routes/         # API Endpoints
│   ├── config/         # DB Connection
├── database/           # SQL scripts and schema
```

- **lofo-app**: Contains the Neo-Brutalist UI and state logic.
- **server**: Handles the REST API, Authentication, and File processing.
- **database**: Contains the `lost_founddb.sql` for setting up the relational engine.

---

## ⚙️ Installation Guide

<details>
<summary><b>Step 1: Clone the Repository</b></summary>

```bash
git clone <repo-url>
cd lofofinal
```
</details>

<details>
<summary><b>Step 2: Frontend Setup</b></summary>

```bash
cd lofo-app
npm install
npm run dev
```
</details>

<details>
<summary><b>Step 3: Backend Setup</b></summary>

```bash
cd server
npm install
npm run dev
```
</details>

<details>
<summary><b>Step 4: Database Setup</b></summary>

1. Open MySQL Workbench or CLI.
2. Create a database: `CREATE DATABASE lost_found_db;`.
3. Import `lost_founddb.sql`.
</details>

---

## 🔐 Environment Variables

Create a `.env` file in the `server/` directory:

```env
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_password
DB_NAME=lost_found_db
JWT_SECRET=your_secret
```

---

## 🔄 Workflow

1.  **Report**: A user reports a Found item in the registry.
2.  **Claim**: Another user finds their item and submits a Claim.
3.  **Proof**: The claimant uploads photographic or documentary evidence.
4.  **Verification**: The claim moves to the "Pending Review" state.
5.  **Adjudication**: An admin reviews the proof and **Approves** or **Rejects**.
6.  **Resolution**: Upon approval, the item is marked as **Closed**.

---

## 🧠 Business Logic

- **Evidence Requirement**: No claim can be processed without valid proof attachments.
- **Admin Adjudication**: Approval is strictly restricted to administrative accounts.
- **Atomic Closure**: Approving one claim automatically rejects all other pending claims for that item.
- **Single Active Claim**: A user can only have one active claim per item at a time.

---

## 📸 Screenshots

| Landing Page | Dashboard |
| :---: | :---: |
| *[Placeholder: Landing Page]* | *[Placeholder: Dashboard]* |

| Claim System | Admin Panel |
| :---: | :---: |
| *[Placeholder: Claim System]* | *[Placeholder: Admin Panel]* |

---

## 👥 Team Members

- **Gagandeep Singh**
- **Sandeep Yadav**
- **Prabhgun Kaur**

---

## 🚀 Future Improvements

- [ ] **Real-time Notifications**: Instant alerts when a claim is reviewed.
- [ ] **AI-based Item Matching**: Automated suggestions based on item descriptions.
- [ ] **Mobile App**: Cross-platform support via React Native.

---

## 📜 License

Distributed under the **MIT License**.
