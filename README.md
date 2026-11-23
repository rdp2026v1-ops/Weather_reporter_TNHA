# Weather Reporter – BK-TNHA

Stand-alone copy of the Weather Reporter web app (Next.js + FastAPI on Vercel) that opens on
**BK-TNHA Platform** by default. All other saved locations remain available in the picker.

## Run locally

```bash
npm install
# put your key in .env:  OPENWEATHERMAP_API_KEY=...
npm run dev:all      # web app on :3000 + Python API on :8000
```

## Deploy

Vercel builds the Next.js app and routes `/api/*` to `api/index.py` (see `vercel.json`).
Set `OPENWEATHERMAP_API_KEY` in the Vercel project's environment variables.

## Changing the default location

Edit `default_location` in `locations.json` **and** `location.json`, and `DEFAULT_NAME` in
`src/hooks/useWeather.ts`.
