# Aurum Estates
https://real-estate-platform-aurum-estate.vercel.app/

**Where extraordinary residences find their owners.**

A discreet collection of villas, penthouses and historic estates, curated for the world's most discerning collectors.

A full-stack MERN real estate platform with search, filters and full property management (create, edit, delete).

## Tech Stack

- **Frontend:** React 18, Vite 5, Tailwind CSS 3, React Router, Axios, Framer Motion
- **Backend:** Node.js, Express, Mongoose
- **Database:** MongoDB

## Quick Start

**Prerequisites:** Node.js 18+ and MongoDB running locally.

```bash
git clone <your-repo-url>
cd Real-Estate-Platform
```

**Backend** (http://localhost:5000)

```bash
cd backend
npm install
copy .env.example .env      # macOS/Linux: cp .env.example .env
npm run seed                # optional: load sample data
npm run dev
```

**Frontend** (http://localhost:5173), in a second terminal

```bash
cd frontend
npm install
copy .env.example .env      # macOS/Linux: cp .env.example .env
npm run dev
```

> Vite reads `.env` only at startup. Restart `npm run dev` after editing it.

## Environment Variables

| File            | Variable        | Default                                  |
|-----------------|-----------------|------------------------------------------|
| `backend/.env`  | `MONGO_URI`     | `mongodb://127.0.0.1:27017/realestateDB` |
| `backend/.env`  | `PORT`          | `5000`                                   |
| `backend/.env`  | `CLIENT_ORIGIN` | `http://localhost:5173`                  |
| `frontend/.env` | `VITE_API_URL`  | `http://localhost:5000/api`              |

## API

Base URL: `http://localhost:5000/api`

| Method | Endpoint          | Description                                                                 |
|--------|-------------------|-----------------------------------------------------------------------------|
| GET    | `/properties`     | List all. Filters: `q`, `type`, `status`, `minPrice`, `maxPrice`, `bedrooms` |
| GET    | `/properties/:id` | Get one                                                                     |
| POST   | `/properties`     | Create                                                                      |
| PUT    | `/properties/:id` | Update                                                                      |
| DELETE | `/properties/:id` | Delete                                                                      |

## Troubleshooting

- **Frontend can't reach API:** check `VITE_API_URL`, then restart the frontend.
- **CORS error:** set `CLIENT_ORIGIN=http://localhost:5173` in `backend/.env`, then restart the backend.
- **Empty listings:** run `npm run seed` in `backend`.

## License

MIT
