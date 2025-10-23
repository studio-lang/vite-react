PITPEcoHandmadeSocial - Starter scaffold
======================================

Overview
--------
This scaffold provides a starter full-stack project for a social layer that imports products/looks
from your existing Base44 site (polling mode). It includes:

- frontend/  -> Next.js + Tailwind (minimal pages)
- backend/   -> Express API (posts, auth placeholder, ai tagging)
- sync/      -> Polling worker that fetches new products from your Base44 page and imports them
- .env.example files and sample scripts
- OpenAI tagging integration placeholder (requires OPENAI_API_KEY)
- NextAuth placeholders for authentication (configure providers in .env)

Important: This is a scaffold — you will need to fill in real keys and connect to Supabase (or your DB).


---
Development notes (new)
-----------------------
1. Run DB migrations against your Postgres/Supabase (migrations/init.sql)
2. Set environment variables in backend/.env and frontend/.env (see .env.example)
3. Start backend:
   cd backend
   npm install
   npm run dev
4. Start frontend:
   cd frontend
   npm install
   npm run dev
5. Start sync worker (separate process):
   cd sync_worker
   npm install
   npm start

Notes:
- The scaffold uses simple demo auth placeholders. NextAuth integration and secure auth flows should be wired with environment provider keys and session middleware.
- For production, secure API endpoints with proper auth and validate incoming webhook payloads.
