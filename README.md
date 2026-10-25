# COD Platform — Cloudflare deployment

This repo is deployed automatically to Cloudflare Workers (free) on every push.

- `worker.js` — the whole platform in one file (built from the source in `source.zip` with `node tools/build-worker.js`).
- `wrangler.toml` — Worker name, D1 database binding (`DB`) and Workers AI binding (`AI`).
- `source.zip` — full source code (Node version runs on a PC with `npm start`).

No secrets are stored in this repo. AI keys are saved inside the platform (Platform → AI keys) in the database.

Update: rebuild `worker.js` from the source, upload it here (replace), Cloudflare redeploys in ~1 minute.
