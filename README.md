# Legal Saathi — source code

A mobile-first bilingual (English/Hindi) Indian legal-awareness website.

## Files
- `index.html` — complete static frontend (HTML, CSS, JavaScript).
- `cloudflare-worker.js` — optional server-side AI endpoint. It is not active until configured and deployed separately.

## Run locally
Open `index.html` in a browser. No build step or package installation is needed.

## Features
- Responsive homepage and navigation
- English/Hindi interface toggle
- Legal topic cards and official resource links
- Local demo chat with a small verified-topic knowledge base
- Law library search
- Procedure guide cards
- Constitution quiz with scoring
- Device-local saved topics

## Important AI note
The chat in `index.html` is explicitly a local demo, not a live AI model. It only responds to a small set of matching topics. Do not present it as live AI. To enable real AI, deploy `cloudflare-worker.js` as a Cloudflare Worker with a Workers AI binding named `AI`, then connect the frontend chat to that endpoint. Keep all service bindings and secrets server-side. Check current Cloudflare model availability and free allocation before relying on it.

The Worker currently allows cross-origin requests from any origin for ease of testing. Before a public launch, restrict `Access-Control-Allow-Origin` to your actual website domain and add abuse controls/rate limits.

## Free static hosting
GitHub Pages can host this static site from a public repository on GitHub Free. Create a repository, upload `index.html`, then go to Settings → Pages → Deploy from a branch → `main` → `/ (root)` → Save. The optional Worker is deployed separately; GitHub Pages does not run server-side code.

## Legal disclaimer
Educational information only; not legal advice. Verify current statutes and procedures from official sources and consult a qualified advocate for a specific matter. Do not enter confidential personal or case information.
