# Drumming Site — Divine Emmanuel

This repository contains a static front-end (`index.html`, `inside.html`, assets) and a minimal Node server (`server/`) to handle bookings and Stripe Checkout webhooks.

Structure
- `index.html`, `inside.html` — front-end booking pages
- `booking-success.html` — post-checkout success page
- `server/` — Node/Express server scaffold (bookings storage, Checkout session creation, webhook, README)

Quick start (local)
1. Serve the static site from `drum_web` root (example):

```bash
cd drum_web
python3 -m http.server 5500
```

2. Start the server for bookings/webhooks:

```bash
cd drum_web/server
npm install
cp .env.example .env   # edit with real values
npm start
```

3. Configure Stripe webhook (see `server/README.md`) and set `DOMAIN` to your site origin.

Deploy
- Push this repository to GitHub and enable GitHub Pages (Settings → Pages) for the `main` branch or `/docs` folder.
