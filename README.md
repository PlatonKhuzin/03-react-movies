# 03-react-movies

React + TypeScript movie search assignment. Styles: https://github.com/goitacademy/react-movies-styles

## Local setup

1. Install Node.js 22.12+ (or a compatible newer version).
2. Copy `.env.example` to `.env`.
3. Set `VITE_TMDB_TOKEN` to your TMDB **API Read Access Token** (the long bearer token, not the API key). Obtain it in your TMDB account API settings: https://www.themoviedb.org/settings/api
4. Run `npm ci`, then `npm run dev`.

Do not commit `.env`. Vite variables are included in the browser build; use the TMDB read token intended for this assignment, never account passwords.

## Checks

`npm run build` — TypeScript and production build.
`npm run format:check` — Prettier.

## Vercel

Import the `03-react-movies` GitHub repository. Framework: Vite. Build: `npm run build`. Output: `dist`. In Environment Variables add `VITE_TMDB_TOKEN` with your API Read Access Token. Deploy. If adding/changing it after deployment, Redeploy is required.
Submit the GitHub URL and the permanent production URL from **Domains** (ending in `.vercel.app`), not the Vercel dashboard URL. Wait 5 minutes after the last push.

## Manual verification

- Empty/whitespace search: `Please enter your search query.` toast and no request.
- Search `Batman`: loader, then cards. Search something nonexistent: old cards clear, empty-results toast.
- Click a card: title, backdrop, overview, release date, rating in a portal.
- Close with X, Escape, backdrop. Body scrolling and focus restore; clicking inside does not close.
- Disable network and search: error message; restore network and search: recovery.
- Submit consecutive searches quickly: only the latest response is displayed.

Live TMDB requests require a valid token. No token is bundled.
