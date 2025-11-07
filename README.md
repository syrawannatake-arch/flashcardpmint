# Wine & Spirit Flashcards (PWA)

A tiny offline-capable flashcards app with images embedded as Base64.

## How to publish on GitHub Pages

### Option A — Deploy with GitHub Actions (recommended)
1. Create a new **public** repository on GitHub (e.g., `flashcards-pwa`).
2. Upload all files from this folder to the repository (keep the `.github/workflows/pages.yml` path).
3. Go to **Settings → Pages** and set:
   - **Source:** `GitHub Actions`
4. Push. The action will publish to Pages automatically.
5. Your site will be available at `https://<your-username>.github.io/<repo-name>/`

### Option B — Simple branch hosting
1. In **Settings → Pages**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`.
2. Commit/push the files. Pages will serve static files without Actions.
3. You can remove `.github/workflows/pages.yml` if you choose this route.

> The app needs to be served over **HTTPS** (GitHub Pages does this) for PWA install to work.

## Dev notes
- All images are embedded; no external requests needed.
- Service Worker (`sw.js`) precaches the core app shell for offline use.
