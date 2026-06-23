# 🚀 QueueLess – Smart Appointment and Token Management System

> Eliminate physical queues. Book appointments, get digital tokens, and track your position in real time.

---

## 🏷️ Project Theme
**Digital Transformation & Public Service Efficiency**

---

## 👥 Team — Runtime Terrors

| Name | TECH ID | Role |
|------|---------|------|
| Ansh Mishra | C15E32 | Founder & Team Lead |
| Pradeep Shukla | C15E1D | Full Stack Developer |
| Aman Singh | C15E25 | Backend Developer |
| Shaurya Verma | C15E55 | Frontend Developer |

---

## 📌 About QueueLess

QueueLess is a smart virtual queue and appointment management system that allows users to book appointments online, receive unique digital tokens, and monitor their queue position in real time — from anywhere, on any device.

**No more standing in lines. No more wasted time.**

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React.js (Vite) |
| Styling | Tailwind CSS |
| Backend | Node.js + Express.js |
| Database | MongoDB + Mongoose |
| Authentication | JWT (JSON Web Tokens) |
| API Testing | Postman |
| Version Control | Git + GitHub |

---

## 📁 Folder Structure

```
QueueLess/
├── frontend/               # React + Vite client
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   └── main.jsx
│   ├── index.html
│   └── package.json
├── backend/                # Node.js + Express server
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── index.js
│   └── package.json
├── README.md
├── PRD.md
├── Contribution.md
└── .gitignore
```

---

## ⚙️ Setup & Run Instructions

### Prerequisites
Make sure you have installed:
- [Node.js](https://nodejs.org/) (v18+)
- [MongoDB](https://www.mongodb.com/) (local or Atlas)
- [Git](https://git-scm.com/)

---

### 1. Clone the Repository
```bash
git clone https://github.com/Pradeep5Shukla/QueueLess.git
cd QueueLess
```

---

### 2. Setup Backend
```bash
cd backend
npm install
```

Create a `.env` file inside the `backend/` folder:
```
PORT=5000
DATABASE_URL=mongodb://127.0.0.1:27017/queuelessDB
JWT_SECRET=your_jwt_secret_key
```

Start the backend server:
```bash
node index.js
```

Backend runs at: `http://localhost:5000`

---

### 3. Setup Frontend
Open a new terminal:
```bash
cd frontend
npm install
npm run dev
```

Frontend runs at: `http://localhost:5173`

---

### 4. Open in Browser
```
http://localhost:5173
```

---

## ✨ Key Features

- 🔐 User Registration & Login (JWT Auth)
- 📅 Appointment Booking with time slots
- 🎫 Digital Token Generation
- 📊 Live Queue Tracking
- 🔔 Turn Notifications
- 🖥️ Admin Dashboard with Analytics

---

## 📄 Documents

- [PRD.md](./PRD.md) — Full Product Requirements Document
- [Contribution.md](./Contribution.md) — Team task allocation and branching strategy

---

## 🔮 Future Enhancements

- AI-based waiting time prediction
- WhatsApp & SMS notifications
- QR code check-in
- Multi-branch support
- PWA (Progressive Web App)

---

> Built with ❤️ by Team Runtime Terrors | TechPreneur 2026 — Gryork Consultants Pvt. Ltd.
