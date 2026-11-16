<h1 align="center">LearnAI</h1>
<p align="center"><b>An adaptive AI learning platform that generates courses, answers questions and quizzes you.</b></p>

<p align="center">
  <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white" />
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" />
  <img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
</p>

## About

LearnAI is my final-year project (Licence ISI, SupMTI, 2025-2026): a full-stack web platform where learners get personalised, AI-generated courses instead of a one-size-fits-all curriculum.

## Features

- **AI course generation**: describe a topic and get a structured course with lessons
- **Course chat**: ask questions about a lesson and get contextual answers
- **Quizzes**: auto-generated quizzes with submission and scoring
- **Authentication**: signup and login with secured passwords
- **PDF export**: download lessons as PDF
- **Vector search ready**: PostgreSQL with the pgvector extension

## Tech stack

| Layer | Technologies |
|-------|--------------|
| Frontend | Next.js 16, React 19, Tailwind CSS, react-markdown, Lucide icons |
| Backend | Python, FastAPI, SQLAlchemy, Pydantic, ReportLab |
| Database | PostgreSQL (pgvector), Redis |
| Infra | Docker Compose |

## Project structure

```
learn-ai/
├── backend/app/
│   ├── main.py          # FastAPI routes
│   ├── core/            # security / auth
│   ├── database/        # models and sessions
│   └── services/        # AI and quiz services
├── frontend/            # Next.js app
└── docker-compose.yml   # PostgreSQL (pgvector) + Redis
```

## Getting started

```bash
# 1. Start PostgreSQL and Redis
docker compose up -d

# 2. Backend
cd backend
python -m venv venv && source venv/bin/activate
pip install fastapi uvicorn sqlalchemy pydantic reportlab
uvicorn app.main:app --reload

# 3. Frontend
cd frontend
npm install
npm run dev
```

The frontend runs on http://localhost:3000 and the API on http://localhost:8000.

## Author

**Adam Ezziyara**, full-stack developer and founder of [AEAgency](https://ae-agency.vercel.app).
