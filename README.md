# srm-client

Service Request Management frontend. React 19, TypeScript, Vite, Tailwind CSS 4.

## Setup

```sh
npm install
npm run dev        # http://localhost:5173
```

The dev server proxies `/api` to `http://localhost:4000`. To use another backend, create `.env.local`:

```
VITE_PROXY_TARGET=http://localhost:8000
```

## Scripts

| Command | Purpose |
|---|---|
| `npm run dev` | Start the dev server |
| `npm run typecheck` | Type-check without emitting |
| `npm run build` | Type-check and build to `dist/` |
| `npm run preview` | Serve the production build locally |

## Environment variables

| Variable | Used for |
|---|---|
| `VITE_API_BASE_URL` | API base URL in production, e.g. `https://<server>.vercel.app/api/v1`. Defaults to `/api/v1`. |
| `VITE_PROXY_TARGET` | Dev-server proxy target (dev only). |
| `VITE_ALLOWED_HOSTS` | Extra comma-separated hosts allowed by the dev and preview servers. |

## Deploy (Vercel)

Framework preset: **Vite**. `vercel.json` sets the build command, output directory and SPA rewrite.
Set `VITE_API_BASE_URL` in the project's environment variables, then deploy.
