# strixtechnical.com

Website for Strix Technical Services LLC, served by Cloudflare Workers (free plan).

- `index.html` is the whole site. Photos and icons sit next to it at the top level.
- Every push to `main` deploys automatically through Cloudflare's GitHub connection (Worker `strix-site`).
- `wrangler.jsonc` tells Cloudflare to serve this folder as static files. `.assetsignore` keeps the repo files (this README, the config) from being served.
- DNS for strixtechnical.com lives in Cloudflare. The domain is still registered at Squarespace.
- The request form posts to a Google Apps Script web app in the Strix Google Drive
  ("Strix Leads" sheet). Its URL is the `FORM_ENDPOINT` value near the bottom of `index.html`.
- Cloudflare's free terms don't allow collecting card numbers on this site. Payments would need a hosted checkout elsewhere.
