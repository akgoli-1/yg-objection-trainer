# Objection Trainer

A spot-the-objection drill for Y&G (Youth & Government) mock trial. The AI shows a
realistic attorney–witness exchange; you decide whether it's objectionable and which
objection applies (or that it's proper). Instant feedback with the rule and how to
phrase the objection out loud.

- Pure drill-and-kill practice with AI-generated scenarios — no upload needed.
- Difficulty levels (Easy / Medium / Hard), running score, and streak (saved in your browser).

## Stack
- Single static `index.html` (no build step).
- `api/chat.js` — Vercel Edge function proxying to Groq (`llama-3.3-70b-versatile`).

## Deploy (Vercel)
1. Push this repo to GitHub.
2. Import it as a new Vercel project.
3. Add an Environment Variable: `GROQ_API_KEY` = your Groq key.
   - Use a key from a **separate Groq account** if you want usage independent of other apps.
4. Deploy. The app is served at `/`, the API at `/api/chat`.

## Embed on a site
Add an iframe whose `src` is the deployed URL. The "← Back to site" button appears
only when embedded and points to `SITE_URL` in `index.html`.
