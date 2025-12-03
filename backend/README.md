# Backend — Fullstack Assignment

Quick overview and endpoints.

## Setup

1. Install dependencies

```powershell
cd backend
npm install
```

2. Create `.env` file or copy from `.env.example` with keys `MONGO_URI`, `JWT_SECRET`, `PORT`.
3. Start server

```powershell
npm run dev
```

## Endpoints
- POST /api/auth/register — { name, email, password }
- POST /api/auth/login — { email, password }
- GET /api/auth/profile — requires Authorization header (Bearer <token>)

Task CRUD (protected)
- GET /api/tasks
- POST /api/tasks — { title, description }
- GET /api/tasks/:id
- PUT /api/tasks/:id — { title, description, completed }
- DELETE /api/tasks/:id

## Notes
- Passwords are hashed using bcrypt
- Authentication uses JWT (7-day expiry)
