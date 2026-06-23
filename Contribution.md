# 🤝 Contribution Guide — QueueLess

**Team:** Runtime Terrors
**Project:** QueueLess – Smart Appointment and Token Management System
**Program:** TechPreneur 2026 | Gryork Consultants Pvt. Ltd.

---

## 👥 Team Members & Roles

| Name | TECH ID | Role |
|------|---------|------|
| Ansh Mishra | C15E32 | Founder & Team Lead |
| Pradeep Shukla | C15E1D | Full Stack Developer |
| Aman Singh | C15E25 | Backend Developer |
| Shaurya Verma | C15E55 | Frontend Developer |

---

## 📋 Feature Distribution & Task Allocation

### Ansh Mishra — C15E32 (Founder & Team Lead)
- Overall project planning and architecture decisions
- Admin Dashboard UI (appointments overview, queue control panel)
- Admin queue management — call next token, update queue progress
- Final integration and testing
- README and documentation review
- **Branch:** `feature/admin-dashboard`

---

### Pradeep Shukla — C15E1D (Full Stack Developer)
- Backend API setup (Express.js server, routing structure)
- JWT Authentication — register, login, token middleware
- Appointment booking API endpoints
- Frontend-backend API integration
- Environment configuration (`.env`, MongoDB connection)
- **Branch:** `feature/auth-and-api`

---

### Aman Singh — C15E25 (Backend Developer)
- MongoDB schema design (Users, Appointments, Tokens, Services)
- Token generation logic and queue position calculation
- Queue status API — real-time position tracking
- Admin analytics endpoints (waiting time reports, service stats)
- API testing with Postman
- **Branch:** `feature/queue-backend`

---

### Shaurya Verma — C15E55 (Frontend Developer)
- React app setup with Vite and Tailwind CSS
- User-facing pages: Home, Register, Login, Dashboard
- Appointment booking UI and form handling
- Live queue status tracker component
- Responsive design across mobile, tablet, and desktop
- **Branch:** `feature/frontend-ui`

---

## 🌿 Git Branching Strategy

```
main
 └── dev                        ← integration branch
      ├── feature/admin-dashboard     (Ansh)
      ├── feature/auth-and-api        (Pradeep)
      ├── feature/queue-backend       (Aman)
      └── feature/frontend-ui         (Shaurya)
```

### Rules:
- ❌ Never push directly to `main`
- ✅ All features go into their own `feature/` branch
- ✅ Merge into `dev` after testing
- ✅ `dev` is merged into `main` only for stable releases
- ✅ Each team member must make regular commits on their branch

---

## 📝 Commit Message Convention

Use clear, descriptive commit messages:

```
feat: add JWT authentication middleware
fix: resolve queue token duplication bug
ui: add appointment booking form
api: create GET /queue/status endpoint
db: add Appointment mongoose schema
docs: update README setup instructions
```

---

## 🔄 Workflow for Each Task

```
1. Pull latest changes:     git pull origin dev
2. Switch to your branch:   git checkout feature/your-branch
3. Make your changes
4. Stage files:             git add -A
5. Commit:                  git commit -m "feat: description"
6. Push:                    git push origin feature/your-branch
7. Create Pull Request → dev on GitHub
```

---

## ✅ Evaluation Note

> Git commit history will be checked during final evaluation.
> All 4 team members must show **active, regular commits** across the 4-day development period.
> Each person must push from their **own GitHub account**.

---

> Team Runtime Terrors | TechPreneur 2026
