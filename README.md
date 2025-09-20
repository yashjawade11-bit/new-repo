# Gravitas Trade Capture - DevOps Guide

## Local dev
1. Copy env: `cp .env.example .env`
2. Start services: `docker compose up --build`
3. Service available at: http://localhost:8000/health

## Tests
Install deps: `pip install -r app/requirements.txt`
Run: `pytest -q`

## CI/CD
- CI runs on push to `dev`/`main`: tests + docker build
- CD: push to `main` triggers GitHub Actions to deploy to staging via SSH

## Troubleshooting
- `docker compose logs -f trade-capture`
- Ensure `.env` exists locally and on staging
