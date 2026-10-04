# ProofHire

ProofHire is a browser-based recruiting screening app: hire on proof, not keywords.

## Project structure

- `index.html` — app shell
- `styles.css` — ProofHire styling
- `app.js` — ProofHire application logic
- `vercel.json` — Vercel SPA/static deployment config
- `netlify.toml` — Netlify deployment config
- `package.json` — optional local development commands

## Deploy

### Vercel
Upload this folder to Vercel, or connect its Git repository. Vercel will serve `index.html` as the app.

### Netlify
Drag the project folder into Netlify Drop, or connect the repository. The included `netlify.toml` handles SPA routing.

### GitHub Pages
Upload the files to a repository and enable GitHub Pages for the repository. Because the app uses hash routes (`#/dashboard`, etc.), it works as a static site.

## Important data behavior

The current app stores the recruiter profile and screening history in browser `localStorage`. That means the interface is deployable and accessible from any device, but the saved profile/history is per browser/device rather than a shared cloud account.

PDF importing still uses the PDF.js CDN on demand. A network connection is therefore required when importing PDFs; pasted text and supported text files do not need PDF.js.
