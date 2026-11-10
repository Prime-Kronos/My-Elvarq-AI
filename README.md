# ELVARQ AI — GitHub Pages edition

Static browser edition of ELVARQ AI.

## Deploy
The GitHub Actions workflow in `.github/workflows/pages.yml` publishes the `site/` folder to GitHub Pages on pushes to `main`.

Expected URL: https://prime-kronos.github.io/My-Elvarq-AI/

## Models
- **Elvarq Beta 1.0** → `llama-3.1-8b-instant`
- **Elvarq Middle 3.4** → `openai/gpt-oss-20b`
- **Elvarq Thinking 4.5** → `openai/gpt-oss-120b`

These are ELVARQ product labels mapped to currently listed Groq model IDs.

## Important security limitation
GitHub Pages is static hosting. It cannot keep a Groq API key secret or run a private backend. This edition asks the user to enter a key at runtime and keeps it only in the current page memory; it is not committed to the repository or saved to local storage. Browser requests expose the key to the browser owner and browser developer tools. Do not use a personal production key in a public/shared kiosk. For a public multi-user service, use a protected server-side API.

This static edition does not include server-side accounts, shared conversation storage, or a secure owner admin panel. Existing backend source is retained in `backend/` but is not deployed by Pages.
