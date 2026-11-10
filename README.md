# ELVARQ AI

A responsive AI assistant web application with a FastAPI backend and server-side Groq integration.

## Stack
- Frontend: vanilla HTML, CSS and JavaScript
- Backend: Python + FastAPI
- Storage: SQLite by default (PostgreSQL-ready deployment configuration)
- AI provider: Groq API, accessed only from the backend

## Model labels
- Elvarq Beta 1.0 — lightweight tier
- Elvarq Middle 3.4 — balanced tier
- Elvarq Thinking 4.5 — advanced tier

These are ELVARQ product labels mapped to provider model IDs in server configuration; they are not claims of independently trained models.

## Run locally
1. `cd backend`
2. `python -m venv .venv && source .venv/bin/activate`
3. `pip install -r requirements.txt`
4. Copy `.env.example` to `.env` and set `GROQ_API_KEY` and `JWT_SECRET`.
5. `uvicorn app:app --reload`
6. Open `http://127.0.0.1:8000`.

Never commit `.env` or expose API keys in frontend code.
