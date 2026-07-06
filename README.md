AI-powered job search assistant — resume ATS scoring, AI resume optimization, resume builder, and application tracking.

Stack: FastAPI + PostgreSQL (backend), Next.js + TypeScript (frontend)

Backend

bashcd backend
cp .env.example.txt .env   # add your DATABASE_URL and SECRET_KEY
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
alembic upgrade head
uvicorn app.main:app --reload --reload-dir app --port 8000

Frontend

bashcd frontend
npm install
echo NEXT_PUBLIC_API_BASE_URL=http://127.0.0.1:8000> .env.local
npm run dev

