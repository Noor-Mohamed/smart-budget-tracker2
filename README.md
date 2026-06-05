# Smart Budget Tracker2 🚀

> **A modern web app that lets users track daily expenses, set monthly budgets, and receive AI‑powered spending insights in real time.**  

---

## 📖 Overview  

Most people only glance at their bank balance **after** they’ve overspent. Smart Budget Tracker2 flips that script by providing a live, category‑based dashboard, proactive alerts, and intelligent suggestions on where to cut back. The goal is to empower users to stay in control of their money **before** the damage happens.

---

## ✨ Features  

| ✅ | Feature | Description |
|---|---|---|
| 📊 | **Live Dashboard** | Real‑time visualization of expenses per category vs. budget. |
| 🔔 | **Budget Alerts** | Push/email notifications when a category approaches its limit. |
| 🤖 | **AI‑Powered Insights** | GPT‑style analysis that suggests spending adjustments based on habits. |
| 🗂️ | **Expense CRUD** | Add, edit, delete, and tag expenses with custom categories. |
| 📅 | **Monthly & Custom Periods** | View reports for any date range (monthly, weekly, custom). |
| 📈 | **Historical Trends** | Graphs showing spending trends over time. |
| 🔐 | **Secure Auth** | JWT‑based authentication with password hashing & optional 2FA. |
| 🌐 | **Responsive UI** | Tailwind‑styled components work on desktop & mobile. |
| 🐳 | **Docker‑Ready** | One‑click dev and production environments via Docker Compose. |

---

## 🛠️ Tech Stack  

| Layer | Technology |
|---|---|
| **Frontend** | React, TypeScript, Tailwind CSS |
| **Backend** | Node.js, Express, TypeScript |
| **Database** | PostgreSQL |
| **AI** | OpenAI / HuggingFace (LLM integration) |
| **Containerisation** | Docker, Docker‑Compose |
| **Testing** | Jest, React Testing Library, Supertest |
| **CI/CD** | GitHub Actions (optional) |

---

## 🚀 Getting Started  

### 1️⃣ Prerequisites  

- **Node.js** ≥ 20.x  
- **Docker** ≥ 24.x & **Docker‑Compose**  
- **Git**  
- **pnpm** (or npm/yarn – pnpm recommended for workspace speed)

### 2️⃣ Clone the repo  

```bash
git clone https://github.com/your‑org/smart-budget-tracker2.git
cd smart-budget-tracker2
```

### 3️⃣ Environment variables  

Copy the example file and fill in your own values (e.g., DB credentials, OpenAI API key).

```bash
cp .env.example .env
# edit .env with your editor
```

### 4️⃣ Run with Docker (recommended)  

```bash
docker compose up --build
```

- Frontend will be available at **http://localhost:3000**  
- Backend API at **http://localhost:4000/api**  
- PostgreSQL at **localhost:5432** (user/password from `.env`)

### 5️⃣ Local development (without Docker)  

```bash
# Backend
cd backend
pnpm install
pnpm dev   # runs ts-node-dev on port 4000

# Frontend
cd ../frontend
pnpm install
pnpm dev   # runs Vite/React on port 3000
```

### 6️⃣ Run tests  

```bash
# Backend tests
cd backend && pnpm test

# Frontend tests
cd ../frontend && pnpm test
```

---

### Recommended Project Structure  

```
smart-budget-tracker2/
├─ .dockerignore
├─ .gitignore
├─ .env.example
├─ docker-compose.yml
├─ README.md
├─ LICENSE
│
├─ backend/
│   ├─ Dockerfile
│   ├─ package.json
│   ├─ tsconfig.json
│   └─ src/
│       ├─ index.ts          # entry point (starts server)
│       ├─ server.ts         # Express app config
│       ├─ routes/
│       │   └─ expense.routes.ts
│       ├─ controllers/
│       │   └─ expense.controller.ts
│       ├─ services/
│       │   └─ aiInsights.service.ts
│       ├─ models/
│       │   └─ expense.model.ts
│       ├─ middleware/
│       │   └─ auth.middleware.ts
│       └─ utils/
│           └─ logger.ts
│
├─ frontend/
│   ├─ Dockerfile
│   ├─ package.json
│   ├─ tsconfig.json
│   ├─ vite.config.ts   # (or next.config.js if using Next.js)
│   └─ src/
│       ├─ main.tsx
│       ├─ App.tsx
│       ├─ routes/
│       │   └─ index.tsx
│       ├─ components/
│       │   ├─ Dashboard/
│       │   │   ├─ index.tsx
│       │   │   ├─ hooks.ts
│       │   │   ├─ types.ts
│       │   │   └─ Dashboard.module.css
│       │   ├─ Expenses/
│       │   └─ Settings/
│       ├─ hooks/
│       │   └─ useAuth.ts
│       ├─ utils/
│       │   └─ api.ts
│       ├─ assets/
│       └─ styles/
│           └─ tailwind.css
│
└─ docs/
    └─ architecture.md
```

*This layout follows the component‑first approach advocated by Robin Wieruch (2026) and keeps backend and frontend concerns clearly separated.*

---

## 📅 Project Timeline  

| Phase | Dates | Milestones |
|---|---|---|
| **Planning & Design** | 2026‑06‑08 → 2026‑06‑20 | Requirements, UI mockups, data model, AI integration plan |
| **Backend MVP** | 2026‑06‑21 → 2026‑07‑10 | Auth, CRUD endpoints, PostgreSQL schema, Dockerfile |
| **Frontend MVP** | 2026‑07‑11 → 2026‑07‑31 | Dashboard UI, Tailwind styling, API client, basic routing |
| **AI Insights Integration** | 2026‑08‑01 → 2026‑08‑15 | LLM wrapper, prompt engineering, real‑time suggestions |
| **Testing & QA** | 2026‑08‑16 → 2026‑08‑31 | Unit & integration tests, end‑to‑end flows, performance profiling |
| **Beta Release & Feedback** | 2026‑09‑01 → 2026‑09‑05 | Deploy to staging, collect user feedback, iterate |
| **Production Launch** | 2026‑09‑06 → 2026‑09‑10 | Final polish, monitoring setup, public release |

---

## 🤝 Contributing  

