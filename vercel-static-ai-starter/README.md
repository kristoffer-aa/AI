# Vercel Static AI Starter (No Framework)

The simplest possible AI site:
- **index.html** (static, easy to tweak)
- **api/chat.js** (serverless function that calls OpenAI securely)
- **vercel.json** (routing/build hints)

## Deploy

1. Push these files to a new GitHub repo.
2. Import the repo into **Vercel** (Framework Preset: **Other**).
3. In Project → **Settings → Environment Variables**, add:
   - `OPENAI_API_KEY` = your key
4. Deploy. Visit your domain.

## Customize

- Edit **index.html** freely (HTML/CSS/JS).
- Server logic lives in **api/chat.js**; you can add more endpoints (e.g., `/api/palette.js`).

## Troubleshooting

- 404 on `/api/chat`: ensure `api/chat.js` exists in the repo root (not nested).
- 500 Missing key: set `OPENAI_API_KEY` in Vercel → Environment Variables.
- Method errors: the page POSTs to `/api/chat` already.
