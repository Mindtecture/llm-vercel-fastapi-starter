# LLM Vercel FastAPI Starter

A minimal, production-ready example of deploying a **FastAPI + OpenAI (LLM)** application to **Vercel** using the Python runtime.

This project is intentionally small and focused. It demonstrates:
- deploying a Python API to Vercel
- calling the OpenAI API from FastAPI
- handling environment variables correctly (local vs production)
- adding a simple health endpoint

It is meant as a **reference project**, not a full application.

---

## Features

- FastAPI backend
- OpenAI API integration
- Serverless deployment on Vercel
- Environment-based configuration (`.env` locally, Vercel env vars in prod)
- Health check endpoint (`/health`)
- Minimal HTML response (no frontend framework)

---

## Endpoints

### `/`
Returns a simple HTML page generated using an LLM.

### `/health`
Lightweight health check endpoint.

Response example:
{
  "status": "ok"
}

---

## Local Development

### 1. Create a virtual environment
python -m venv .venv
source .venv/bin/activate
Windows: .venv\Scripts\activate

### 2. Install dependencies
pip install -r requirements.txt

### 3. Set environment variables
Create a `.env` file with:
OPENAI_API_KEY=your_api_key_here

### 4. Run locally
uvicorn instant:app --reload

Then open:
http://127.0.0.1:8000

---

## Deployment

This project is deployed on **Vercel** using the Python runtime.

Key points:
- `vercel.json` defines the build and routing
- Environment variables are configured via the Vercel dashboard
- No `.env` file is used in production

---

## Why this project exists

This repository serves as:
- a learning exercise
- a clean reference for LLM + serverless deployment
- a minimal public example without unnecessary complexity

It intentionally avoids frontend frameworks and advanced features so the core deployment pattern remains easy to understand.

---

## License

MIT
