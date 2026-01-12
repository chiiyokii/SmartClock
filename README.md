# DevOps Lab – Student Project (Node.js + Jira/GitHub + CI/CD)

This repository is a **teaching template** for a 4-student DevOps mini-project. It contains an **Express** backend and a **Vite** frontend.

---

## Quick start (install & run) ✅

Prerequisites:
- Node.js (v16+ recommended)
- npm (bundled with Node)
- A MongoDB instance (local or hosted). You'll need a `MONGO_URI` connection string.

1) Clone the repo (if you haven't):

```bash
git clone <repo-url>
cd SmartClock
```

2) Backend – install & run:

```bash
cd backend
# install dependencies
npm install

# create a .env file (copy .env example if present) and set at least:
# MONGO_URI, FRONTEND_URL, PORT, JWT_SECRET, JWT_EXPIRES_IN
# Example:
# MONGO_URI=mongodb+srv://<user>:<pass>@cluster.mongodb.net/?authSource=admin
# FRONTEND_URL=http://localhost:5173
# PORT=3000
# JWT_SECRET=super_secret_change_me
# JWT_EXPIRES_IN=7d

# Run in development (with nodemon):
npm run dev

# or run normally:
npm start
```

- The backend listens on `http://localhost:3000` by default.
- Quick health check: `curl http://localhost:3000/health` should return 200.

3) Frontend – install & run:

```bash
cd ../frontend
npm install
npm run dev
```

- The frontend uses Vite, default URL: `http://localhost:5173`.
- Ensure `FRONTEND_URL` in the backend `.env` matches the URL where the frontend is served (defaults to `http://localhost:5173`).

4) Open the app in your browser at `http://localhost:5173` and verify the backend logs for socket connections and API requests.

---

## Tests (optional)

- If the project includes tests, run them from the backend folder:

```bash
cd backend
npm test        # if test script is configured
npm test -- --coverage
```

Note: Some starter templates include Vitest + Supertest for integration and unit tests.

---

## Useful commands & tips 💡

- Install a missing dependency: `npm install <package>` inside the correct package folder (`backend` or `frontend`).
- If the backend fails to start, verify:
  - `.env` contains a valid `MONGO_URI`
  - the MongoDB instance is reachable
  - required packages are installed (`npm install`)
- To inspect logs: check the terminal running `npm run dev` for backend and frontend terminals.

---

## Project layout

```
backend/    # Express API (run on :3000)
frontend/   # Vite + React/Preact UI (run on :5173)
```

---

If you want, I can also add a minimal `backend/.env.example` and a short script to bootstrap both services.

Enjoy the project! 🚀
