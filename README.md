# 🏢 1Clik HR Management System

[![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)](https://www.mongodb.com/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)](https://vitejs.dev/)

> A powerful, full-stack HR management ecosystem designed for modern teams. Streamline directory management, attendance tracking, and leave workflows with a sleek, glassmorphic UI.

---

## ✨ Key Features

- 🔐 **Secure Authentication**: Multi-flow login with Email/Password (verification included) and Google OAuth 2.0.
- 👥 **Employee Directory**: Centralized management for admins to list, search, and onboard team members.
- ⏱️ **Live Attendance**: Real-time check-in system with persisted logging and role-based access.
- 📅 **Leave Management**: Seamless submission and approval workflow for employee time-off requests.
- 📊 **Smart Dashboard**: High-level summary cards for team health and operational insights.
- 🛡️ **Granular RBAC**: Strict role-based access control for `Admin` and `Employee` tiers.

---

## 🛠️ Technology Stack

### **Frontend**
| Tool | Purpose |
| :--- | :--- |
| **React 19** | Modern UI library with concurrent rendering |
| **Tailwind CSS 4** | High-performance, utility-first styling |
| **Vite** | Lightning-fast build tool and dev server |
| **React Router** | Client-side navigation |
| **Axios** | Robust API communication |

### **Backend**
| Tool | Purpose |
| :--- | :--- |
| **Node.js** | Scalable server-side execution |
| **Express 5** | Minimalist web framework for APIs |
| **Mongoose** | Elegant MongoDB object modeling |
| **JWT & Bcrypt** | Industry-standard security and hashing |
| **Nodemailer** | Automated email dispatching |

---

## 📁 Project Architecture

```text
hr-management/
├── 📂 backend/           # Express API & MongoDB Models
│   ├── 🛠️ middleware/    # Auth & Admin validation
│   ├── 📑 models/        # Mongoose schemas
│   └── 🔌 routes/        # API endpoints
├── 📂 frontend/          # React + Vite Dashboard
│   ├── 🎨 src/           # UI Logic & Components
│   └── ⚙️ vite.config.js  # Build configurations
└── 📄 package.json       # Workspace scripts
```

---

## 🚀 Quick Start

### 1. Installation
Install dependencies for all workspaces from the root:
```bash
npm install
npm install --prefix backend
npm install --prefix frontend
```

### 2. Configuration
Create your `.env` files based on the templates:

**Backend (`backend/.env`)**
```env
PORT=5000
MONGO_URI=mongodb://127.0.0.1:27017/hrm
JWT_SECRET=your_jwt_secret
```

**Frontend (`frontend/.env`)**
```env
VITE_GOOGLE_CLIENT_ID=your_id.apps.googleusercontent.com
VITE_API_BASE_URL=http://localhost:5000
```

### 3. Execution
Run both apps concurrently with one command:
```bash
npm run dev
```

- **Frontend**: [http://localhost:5173](http://localhost:5173)
- **API**: [http://localhost:5000](http://localhost:5000)

---

## 🔌 API Reference Summary

| Method | Endpoint | Access | Description |
| :--- | :--- | :--- | :--- |
| `POST` | `/api/auth/login` | Public | Login & get JWT |
| `POST` | `/api/auth/google` | Public | Google OAuth Login |
| `GET` | `/api/employees` | Auth | List all employees |
| `POST` | `/api/employees` | Admin | Create new employee |
| `POST` | `/api/attendance/checkin` | Auth | Log daily check-in |
| `PUT` | `/api/leaves/:id/status` | Admin | Approve/Reject leave |

---

## 🧪 Seeding Demo Data
To quickly test the application with sample data:
```bash
cd backend
node seed.js
```
*   **Admin Email**: `admin@oneclick.com`
*   **Default Password**: `admin123`

---

## 📝 License
Distributed under the **ISC License**. See `LICENSE` for more information.

---
Built with ❤️ by [Mayank](https://github.com/mayankdoel)
