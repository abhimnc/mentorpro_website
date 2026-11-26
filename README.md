# mentorpro.in

Static marketing site for the ProMentors app, hosted on GitHub Pages. No build step.

| File | Purpose |
|---|---|
| `index.html` | Landing page |
| `privacy-policy.html` | Privacy policy (linked from the Play Store listing) |
| `404.html` | Not-found page |
| `CNAME` | Custom domain for GitHub Pages (`mentorpro.in`) |
| `.nojekyll` | Serve files as-is, skip Jekyll |

## Deploy

1. Push this folder's contents to the root of a **public** GitHub repo (e.g. `mentorpro-site`).
2. Repo → Settings → Pages → Source: *Deploy from a branch*, Branch: `main`, folder `/ (root)`.
3. At your DNS provider for `mentorpro.in`, add:
   - `A` records for `@` → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` for `www` → `<your-github-username>.github.io`
   - Leave the existing `api` record alone (it points at the backend).
4. Back in Settings → Pages, wait for the DNS check, then tick **Enforce HTTPS**.

To preview locally: `python3 -m http.server 8000` in this folder, then open http://localhost:8000.
