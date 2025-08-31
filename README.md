# myQRflow Support Site

Static site for myQRflow support, privacy policy, and basic product info. Published via GitHub Pages.

## Contents
- `index.html` – simple landing page with links to Support and Privacy
- `support/index.html` – FAQs and contact info
- `privacy.html` – privacy policy
- `CNAME` – custom domain configuration (currently `support.myqrflow.com`)

## Edit and update
1. Make changes to the HTML files.
2. Commit and push to `main`:
   ```bash
   git add -A
   git commit -m "Update site content"
   git push
   ```
3. GitHub Pages will redeploy automatically in ~1–3 minutes.

## Local preview
Serve the folder locally to test changes:
```bash
# Option 1: Python 3
python3 -m http.server 8080
# Option 2: Node (if installed)
npx serve -l 8080
```
Open `http://localhost:8080` in your browser.

## GitHub Pages deployment
- Repository Settings → Pages
  - Source: Deploy from a branch
  - Branch: `main`, Folder: `/ (root)`
- For a custom domain, set the “Custom domain” to `support.myqrflow.com` and enable “Enforce HTTPS”.

## DNS (Route 53)
Create a `CNAME` record in the `myqrflow.com` hosted zone:
- Name: `support`
- Type: `CNAME`
- Value: `<your-username>.github.io.`
- TTL: `300`

Note: The `CNAME` file in this repo must match the custom domain you set in GitHub Pages. Update the file if you change domains.

## License
All rights reserved. Content is proprietary to the myQRflow project.



