# Realtime Spotify Clone ✨

![Demo App](/frontend/public/screenshot-for-readme.png)

A realtime music web application with chat, live presence, and an admin dashboard for managing albums and songs. This repo contains a Node.js/Express backend and a TypeScript/Vite React frontend.


## Features

- Play, pause, next/previous track controls
- Volume control and playback UI
- Admin dashboard: create albums and upload songs
- Real-time chat and presence (see who is online)
- Analytics page with aggregated statistics
- File uploads via Cloudinary

## Tech stack

- Backend: Node.js, Express, MongoDB
- Frontend: React, TypeScript, Vite, TailwindCSS
- Realtime: WebSocket (socket.io)
- Auth: Clerk (configurable)

## Prerequisites

- Node.js 18+ and npm/yarn
- MongoDB instance (local or Atlas)
- Cloudinary account (for uploads)

## Quickstart

1. Install dependencies for both backend and frontend.

```bash
# from project root
cd backend && npm install
cd ../frontend && npm install
```

2. Create environment files.

- Backend: create `backend/.env` with the variables listed in the Backend env section below.
- Frontend: create `frontend/.env` with the variables listed in the Frontend env section below.

3. Start backend and frontend in separate terminals.

```bash
# start backend (from /backend)
npm run dev

# start frontend (from /frontend)
npm run dev
```

Open the app at the address printed by Vite (typically http://localhost:5173).

## Backend env (backend/.env)

Example variables required by the backend:

```
PORT=4000
MONGODB_URI=mongodb+srv://<user>:<pass>@cluster0.mongodb.net/spotify_clone
NODE_ENV=development
ADMIN_EMAIL=admin@example.com

# Cloudinary
CLOUDINARY_API_KEY=...
CLOUDINARY_API_SECRET=...
CLOUDINARY_CLOUD_NAME=...

# Clerk (optional)
CLERK_PUBLISHABLE_KEY=...
CLERK_SECRET_KEY=...
```

## Frontend env (frontend/.env)

```
VITE_CLERK_PUBLISHABLE_KEY=...
```

## Seed data

The repository includes seed files under `backend/src/seeds` for albums and songs. To import them, run any provided seed scripts (or use a small script to load the JSON into MongoDB).

## Project structure (high level)

- `backend/` — Express server, API routes, models, sockets
- `frontend/` — React + Vite application and UI components

## Useful scripts

- `backend/package.json`:
	- `npm run dev` — start backend in development
	- `npm run seed` — (if available) seed database
- `frontend/package.json`:
	- `npm run dev` — start Vite dev server
	- `npm run build` — build production bundle

## Contributing

Pull requests are welcome. For major changes, open an issue first to discuss what you would like to change.


- Add a one-command `start` script to run both backend and frontend concurrently
- Add a short development checklist for common env values

Tell me which additions you'd like and I'll update the README accordingly.
