# Pinteria 🍺

An AI cicerone in your pocket — ask anything about beer, whisky, wine, and spirits and get expert answers instantly. Built as a single static page with a Vercel serverless function proxying to the Gemini API, so the API key never touches the browser.

**Live:** _add your deployed URL here_

## Stack

- Static HTML/CSS/JS (no build step, no framework)
- Vercel serverless function (`api/chat.js`) proxying to the Gemini API
- Procedural Web Audio background music (no audio files)

## Local development

1. Clone the repo and copy `.env.example` to `.env.local`, filling in a [Gemini API key](https://aistudio.google.com/apikey).
2. Run with the [Vercel CLI](https://vercel.com/docs/cli): `vercel dev`
3. Open the printed local URL — the app is served from `index.html` with `/api/chat` proxied by the CLI.

## Deploying

Push to GitHub and import the repo in Vercel, or run `vercel --prod`. Set `GEMINI_API_KEY` under Project Settings → Environment Variables before deploying.