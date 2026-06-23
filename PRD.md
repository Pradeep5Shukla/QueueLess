# Product Requirements Document (PRD)

## Project Title
**QueueLess – Smart Appointment and Token Management System**

**Prepared By:** Team RunTime Terror
**Date:** 22-06-2026

---

## 1. Introduction

Have you ever visited a hospital, bank, or government office and spent hours waiting for your turn? Long queues are frustrating and often waste a lot of time. In many places, people still have to stand in physical lines without knowing when they will be served.

QueueLess is designed to solve this problem by providing a smart appointment and token management system. Instead of waiting in a crowded area, users can book appointments online, receive digital tokens, and track their position in the queue in real time.

The goal is to make the waiting experience more organized, transparent, and convenient for both customers and service providers.

---

## 2. Problem Statement

Traditional queue management methods create several challenges:

- Customers spend a lot of time waiting in physical queues.
- Waiting areas become overcrowded and uncomfortable.
- Staff members struggle to manage large numbers of visitors efficiently.
- People have no clear idea about their expected waiting time.
- Manual token systems are prone to errors and confusion.

These issues affect customer satisfaction and reduce operational efficiency across hospitals, banks, government offices, and educational institutions.

---

## 3. Market Research

Queue management has become increasingly important as businesses and public service organizations move towards digital transformation.

Several organizations such as hospitals, banks, and service centers have started using digital queue systems to improve customer experience. Existing solutions offer online appointments and virtual queues, but many are expensive or designed primarily for large enterprises.

### Competitor Analysis

| Competitor | Features | Limitation |
|------------|----------|------------|
| Qminder | Virtual queues, customer notifications | Higher pricing for small businesses |
| Waitwhile | Appointment scheduling, waitlist management | Subscription costs can be high |
| NextMe | Queue tracking and customer updates | Limited customization options |
| Skiplino | Token management and analytics | Mainly targets large organizations |

### Opportunity

There is a clear need for an affordable and easy-to-use solution that can serve small clinics, educational institutions, and local businesses. QueueLess aims to fill this gap with a lightweight, open, and scalable digital queue system.

---

## 4. Target Users

### Primary Users
- Patients visiting hospitals or clinics
- Customers visiting banks
- Citizens accessing government services
- Students visiting college administration offices

### Secondary Users
- Reception staff and service agents
- Business administrators and managers

---

## 5. Product Goals

1. Reduce customer waiting time significantly.
2. Minimize overcrowding in waiting areas.
3. Improve customer satisfaction through transparency.
4. Simplify queue management for staff.
5. Provide real-time updates and notifications.

---

## 6. Key Features (MVP)

### For Customers
- **User Registration and Login** — Secure account creation and authentication.
- **Appointment Booking** — Select a service and book an available time slot.
- **Digital Token Generation** — Unique token number auto-generated after booking.
- **Live Queue Tracking** — Real-time position in the queue visible anytime.
- **Notifications** — Alerts sent when the user's turn is approaching.
- **Appointment History** — View previous appointments and bookings.

### For Administrators
- **Dashboard** — Overview of appointments, active queues, and counters.
- **Queue Management** — Call next token, manage waiting customers.
- **Appointment Control** — Approve, modify, or cancel appointments.
- **Analytics** — Reports on waiting times and service performance.

---

## 7. Functional Requirements

### User Side
- Users must be able to register and log in securely.
- Users must be able to book, cancel, or reschedule appointments.
- Users must receive a unique token number upon booking.
- Users must be able to view real-time queue status.

### Admin Side
- Admins must be able to manage appointments and service counters.
- Admins must be able to update queue progress.
- Admins must be able to access reports and analytics.

---

## 8. Non-Functional Requirements

- The system should maintain **99% uptime** availability.
- Pages should **load within 2 seconds** under normal conditions.
- All user data must be **securely stored** with encrypted credentials.
- The application must be **fully responsive** across mobile, tablet, and desktop.
- The architecture must support **future scalability**.

---

## 9. Tech Stack

| Layer | Technology | Purpose |
|-------|-----------|---------|
| **Frontend** | React.js (Vite) | Fast, component-based UI |
| **Styling** | Tailwind CSS | Responsive, utility-first design |
| **Backend** | Node.js + Express.js | RESTful API server |
| **Database** | MongoDB + Mongoose | Flexible NoSQL data storage |
| **Authentication** | JWT (JSON Web Tokens) | Secure, stateless user sessions |
| **API Testing** | Postman | API development and testing |
| **DB Management** | MongoDB Compass | Visual database management |
| **Version Control** | Git + GitHub | Collaboration and code versioning |
| **Dev Environment** | VS Code | Code editor |

---

## 10. Technical Overview

### System Architecture

QueueLess follows a **client-server architecture** with a clear separation between the frontend and backend:

```
User Browser
     │
     ▼
React Frontend (Vite) ──── REST API calls ────► Express.js Backend
     │                                                  │
     │                                                  ▼
     │                                           MongoDB Database
     │                                          (tokens, users, queues)
     ▼
JWT Authentication (stored in localStorage)
```

### How It Works

1. **Frontend (React + Vite):** A Single Page Application (SPA) that communicates with the backend via REST API calls. React Router handles navigation between pages. Tailwind CSS ensures a clean, responsive UI.

2. **Backend (Node.js + Express.js):** Handles all business logic — user authentication, token generation, queue management, and appointment scheduling. Organized into routes, controllers, and models following MVC pattern.

3. **Database (MongoDB):** Stores all data in collections:
   - `users` — customer and admin accounts
   - `appointments` — booking details and status
   - `tokens` — queue tokens with real-time position tracking
   - `services` — available service types per organization

4. **Authentication (JWT):** On login, the server issues a signed JWT token. The frontend includes this token in every API request header for secure, stateless authorization.

5. **Queue Logic:** When a user books an appointment, the system auto-generates a token number, calculates estimated wait time based on active queue length, and updates queue positions in real time.

### API Structure (REST)

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/auth/register` | User registration |
| POST | `/api/auth/login` | User login |
| GET | `/api/queue/status` | Get live queue status |
| POST | `/api/appointments/book` | Book appointment |
| PUT | `/api/appointments/:id` | Update appointment |
| DELETE | `/api/appointments/:id` | Cancel appointment |
| GET | `/api/admin/dashboard` | Admin dashboard data |

### Folder Structure

```
QueueLess/
├── frontend/               # React + Vite client
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/          # Route-level pages
│   │   ├── services/       # API call functions
│   │   └── main.jsx        # Entry point
│   └── package.json
├── backend/                # Node.js + Express server
│   ├── controllers/        # Business logic
│   ├── models/             # Mongoose schemas
│   ├── routes/             # API route definitions
│   ├── middleware/         # Auth middleware (JWT)
│   ├── .env                # Environment variables (gitignored)
│   └── index.js            # Server entry point
├── README.md
├── PRD.md
├── Contribution.md
└── .gitignore
```

---

## 11. User Journey

1. User registers or logs in to QueueLess.
2. User selects the desired service (e.g., hospital, bank).
3. User books an appointment for a specific time slot.
4. System generates a unique digital token.
5. User monitors queue status remotely from any device.
6. User receives a notification when their turn is approaching.
7. User visits the service counter when called.
8. Service is completed and appointment marked as done.

---

## 12. Success Metrics

- Reduction in average customer waiting time.
- Number of appointments successfully completed per day.
- Customer satisfaction ratings (target: 4+ stars).
- Reduction in physical crowding at service locations.
- Growth in active users and organizations onboarded.

---

## 13. Future Enhancements

- AI-based waiting time prediction
- WhatsApp and SMS notifications
- QR code check-in at service counters
- Multi-branch management for large organizations
- Voice assistant support
- Integration with payment systems
- Progressive Web App (PWA) support for offline access

---

## 14. Conclusion

QueueLess aims to modernize the traditional waiting experience by replacing physical queues with a smart digital solution. Built on a modern MERN stack (MongoDB, Express, React, Node.js), the system is designed to be lightweight, scalable, and accessible to organizations of all sizes.

By enabling appointment booking, virtual tokens, and real-time queue tracking, QueueLess can save time, improve customer satisfaction, and help organizations operate more efficiently — from small local clinics to large government offices.
