# Restaurant Reservations

A full-stack restaurant reservation system with customer and admin support.

## Structure

- `backend/server/`: Express backend with MongoDB, JWT auth, role-based authorization, and seed scripts
- `frontend/`: React + Vite frontend with separate customer and admin dashboards

## Requirements Covered

- JWT login/register
- MongoDB persistence with Mongoose
- Role-based admin and customer dashboards
- Customer reservation creation, viewing, and cancellation
- Admin reservation management, date filtering, update, cancellation, and table management
- Automatic table assignment and capacity validation
- Prevents double booking for active reservations
- Docker support
- API-ready backend for Render deployment
- Frontend ready for Vercel deployment

## Backend setup

1. Copy the example env file:

```bash
cd backend/server
cp .env.example .env
```

2. Install dependencies and start the backend:

```bash
npm install
npm run dev
```

3. Seed the database with demo users and tables:

```bash
npm run seed
```

4. Backend runs at: `http://localhost:5000`

## Frontend setup

1. Copy the example env file:

```bash
cd frontend
cp .env.example .env
```

2. Install dependencies and start the frontend:

```bash
npm install
npm run dev
```

3. Open the frontend at `http://localhost:5173`.

## Seed Accounts

- Admin: `admin@restaurant.com` / `admin123`
- Customer: `guest@restaurant.com` / `guest123`

## Docker

Build and run everything locally with Docker Compose:

```bash
docker compose up --build
```

## Deployment

- Backend: deploy with Render or any Node.js service that supports environment variables
- Frontend: deploy with Vercel using `vercel.json`

## Postman

Use `postman_collection.json` in the repo root to test the API endpoints.

## Notes

- The backend uses `MONGO_URI`, `JWT_SECRET`, and `PORT` from `.env`
- The frontend uses `VITE_API_URL` from `.env`
- Admin users can manage tables and all reservations
- Customers can only manage their own reservations
