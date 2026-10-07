# Paperlens (installable web app)

Understand any research paper fast: overview, key figures, mind map, flashcards, games and chat.

## Put it online with GitHub Pages (about 5 minutes, free)

1. Sign in at https://github.com (create a free account if needed).
2. Click **+** (top right) → **New repository**.
   - Name: `paperlens` (any name works)
   - Choose **Public** (free GitHub Pages needs a public repository)
   - Click **Create repository**
3. On the new empty repo page, click **uploading an existing file**.
4. Open the unzipped `paperlens-pwa` folder, select **all the files inside it**
   (`index.html`, `sw.js`, `manifest.webmanifest`, the icon files, and this README),
   and drag them into the browser. Click **Commit changes**.
5. Go to **Settings → Pages**. Under **Build and deployment**, set
   **Source: Deploy from a branch**, **Branch: main**, folder **/ (root)**, then **Save**.
6. Wait about a minute and refresh. GitHub shows your address:
   `https://YOUR-USERNAME.github.io/paperlens/`

## Install it

- **Chrome or Edge (desktop):** open your address, then click the install icon in the address bar
  or the **Install app** button inside Paperlens.
- **Android (Chrome):** open your address, tap **Install app** (or menu → Install app).
- **iPhone / iPad (Safari):** open your address, tap **Share → Add to Home Screen**.

## First use

Open **Settings** (gear icon) and paste your Anthropic API key. It is saved only in your browser on that device.
Each device needs its own key. Papers are sent directly to Anthropic and nowhere else.

## Updating later

Upload the new `index.html` to the same repository (Add file → Upload files, same name) and commit.
Open the app twice to pick up the new version.

## Good to know

- The app opens offline, and saved papers can be read offline. Analysing a paper and chat need internet.
- Anyone with your address can open the app, but each person needs their own API key.
- Never put your API key in the files or in the repository.
