# FuelEU Compliance Dashboard
A full-stack web application that calculates and visualizes maritime fuel GHG compliance based on FuelEU Maritime Regulation (EU 2023/1805).
---
## 🚢 Overview
This tool allows users to:
- View vessel route emissions
- Compare GHG Intensity values against baseline routes
- Compute yearly **Compliance Balance (CB)**
- Perform **Banking** of surplus CB
- Create **Pooling** groups to reassign surplus between ships

Built according to **Hexagonal Architecture**:
core (domain + logic)
↑ ↓
ports (interfaces)
↑ ↓
adapters (Express + React UI, Prisma ORM)
---
## 🧱 Tech Stack
| Layer | Technology |
|------|------------|
| Frontend | React + TypeScript + Vite + Tailwind |
| Backend | Node.js + Express + TypeScript |
| Database | PostgreSQL |
| ORM | Prisma ORM |
| State & Data Fetching | TanStack React Query |
---
## 📦 Setup Instructions
### 1. Clone repository
git clone <your_repo_url>
cd project-root
### 2. Backend Setup
cd backend
cp .env.example .env # ensure DATABASE_URL is correct
npm install
npx prisma migrate dev
npm run seed
npm run dev

Backend will run at:
http://localhost:3000

### 3. Frontend Setup
cd frontend
npm install
npm run dev

Frontend runs at:
http://localhost:5173
---
## 🔌 API Endpoints
| Method | Route | Description |
|--------|-------|-------------|
| GET | `/routes` | List routes |
| POST | `/routes/:id/baseline` | Set baseline |
| GET | `/routes/comparison` | Baseline vs others |
| GET | `/compliance/cb` | Compute Compliance Balance |
| POST | `/banking/bank` | Bank surplus |
| POST | `/banking/apply` | Apply bank |
| POST | `/pools` | Create pooling allocation |
---
## ✅ Tests
Run:
npm run test

## 📸 UI Preview
![Screenshot_8-11-2025_02336_localhost](https://github.com/user-attachments/assets/d02112e9-6533-41a5-904c-e4ccf4f117f5)
![Screenshot_8-11-2025_0239_localhost](https://github.com/user-attachments/assets/58adad81-abf2-4988-8e7d-debee91c8410)
![Screenshot_8-11-2025_02216_localhost](https://github.com/user-attachments/assets/6bbb68cd-21f2-49be-873c-9e95d9c8a21f)
![Screenshot_8-11-2025_02114_localhost](https://github.com/user-attachments/assets/b6bff713-5d8e-4166-9ef0-adf7299356be)




