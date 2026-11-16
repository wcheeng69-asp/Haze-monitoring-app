# Haze Watch

Single-page app showing Singapore PSI by area (NEA, via data.gov.sg) and current weather for Singapore and ASEAN cities (Open-Meteo). No build step, no dependencies.

## Data sources
- Haze: `https://api-open.data.gov.sg/v2/real-time/api/psi` (Singapore only). If the request fails, the page shows a saved NEA reading and says so in the footnote.
- Weather: `https://api.open-meteo.com/v1/forecast` for every city. If it fails, the weather cards show an unavailable message.
- Both refresh every 15 minutes.

## Deploy to Vercel
1. Push this folder to a GitHub repository (`index.html` at the repo root).
2. In Vercel, choose Add New > Project, import the repository.
3. Framework Preset: Other. Leave Build Command and Output Directory empty. Deploy.

Or from the terminal: `npx vercel --prod`.

## Run locally
Open `index.html` in a browser, or run `npx serve .`.
