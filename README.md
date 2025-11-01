# Fintech Playground (Vercel-ready)

This repository is a monorepo intended to be deployed on **Vercel** as a single project:
- Frontend: `frontend/` — Vite + React app (static build)
- Backend: `api/` — Python serverless functions (mocked payments; no external API keys needed)

Deployment steps (quick):
1. Zip and upload repository to GitHub, or use `Upload` on Vercel and connect GitHub repo.
2. On Vercel, import the project. The `vercel.json` is configured to:
   - Build the React frontend using `@vercel/static-build`
   - Expose Python files in `api/` as serverless functions with `@vercel/python`
3. Deploy. After deployment the frontend will be served and API routes available under `/api/*`.

Local testing (frontend):
- `cd frontend && npm install && npm run dev`

Notes:
- The Python API uses simple mock implementations for payments and lending to work without API keys.
- If you prefer a Flask backend deployment elsewhere (Render/Railway), the `api/` handlers can be adapted to Flask quickly.
