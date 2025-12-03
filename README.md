# Fullstack Project — Frontend Intern Assignment Template

This repository is a full-stack assignment template suitable for a Frontend Developer Intern. It includes a React + Tailwind frontend and an Express + MongoDB backend with JWT authentication and task CRUD APIs.

## Features
- Auth: Register, Login with JWT
- Backend: Node.js/Express, MongoDB, bcrypt for hashing, JWT for tokens
- Frontend: React, Tailwind CSS, Protected routes, Axios, basic CRUD UI

## Folder Structure

- backend/: Express server
  - src/
    - app.js: App setup and route mounting
    - server.js: Server bootstrap
    - config/db.js: MongoDB connection
    - controllers/: auth and task controllers
    - middleware/auth.js: JWT middleware
    - models/: User and Task models
    - routes/: api routes

- frontend/: React + Vite app
  - src/
    - api/axios.js: Axios instance with Authorization header
    - components/: ProtectedRoute, Navbar
    - context/: AuthContext for global auth state
    - pages/: Register, Login, Dashboard, NotFound

## Getting Started

### Backend

1. Install dependencies:

```powershell
cd backend
npm install
```

2. Create `.env` (visit `.env.example` for keys):

```powershell
# .env
MONGO_URI=mongodb://localhost:27017/fullstack-db
JWT_SECRET=change_this_secret
PORT=5000
```

3. Start server:

```powershell
npm run dev
```

### Frontend

1. Install dependencies:

```powershell
cd frontend
npm install
```

2. Create `.env` (visit `.env.example`):

```powershell
VITE_API_URL=http://localhost:5000/api
```

3. Start dev server:

```powershell
npm run dev
```

## API endpoints

- POST /api/auth/register — Register a new user (body: name, email, password)
- POST /api/auth/login — Login (body: email, password)
- GET /api/auth/profile — Get current user (protected)
- GET /api/tasks — Get user tasks (protected)
- POST /api/tasks — Create task (protected)
- GET /api/tasks/:id — Get a task (protected)
- PUT /api/tasks/:id — Update a task (protected)
- DELETE /api/tasks/:id — Delete a task (protected)

---

If you want to extend this template, consider adding:
- Input validation (Joi or express-validator)
- Better error handling and logging
- Role management and permissions
- Docker or docker-compose for dev environment

Good luck, and feel free to reach out if you'd like this repo trimmed to a challenge level or a student assignment checklist.
