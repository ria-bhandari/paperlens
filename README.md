# Paperlens

**Understand any research paper in minutes.** Drop in a PDF and get a clear overview, the figures that matter, an interactive mind map, flashcards, three games, and a chat that answers questions about the paper. Works for any field.

**Live app:** `https://YOUR-USERNAME.github.io/paperlens/` *(replace with your own address once it's deployed)*

---

## What you get

| Tab | What it does |
|---|---|
| **Overview** | A TL;DR, a "worth a full read if…" line, a snapshot (study type, data, method, headline result), key findings with numbers, the problem and approach, a plain-English version, caveats, and a glossary. Each finding links to the PDF page it came from. |
| **Figures** | The 3 to 6 figures and tables that carry the paper, shown as the real PDF page, each with what it shows, why it matters, a one-line takeaway, and a "Look closely" prompt for reading critically. |
| **Mind map** | An interactive map you can pan, zoom, expand and collapse. Click a node to read its note. Export as SVG or PNG for slides. |
| **Flashcards** | Flip cards with *Show again soon*, *Hard, later* and *I know this*. Filter by type (concepts, methods, results, terms, critique). Export to Anki. |
| **Play** | **Quiz blitz** (lives, a timer and streak bonuses), **Fact or fiction**, and **Pair up** (match terms to meanings against the clock). Questions you miss can be turned into flashcards in one click. |
| **Chat** | Ask anything about the paper. Answers are grounded in the full PDF, and page references open the page so you can check them. |

Also: six themes (Paper, Spring, Golden hour, Fall, Winter, Dusk) with light and dark modes and an optional "follow the seasons" setting, a saved library of past papers, Markdown notes export, and an "explain it for" setting (nearby-field researcher, specialist, or newcomer).

---

## How it works

```
 your browser                                   Anthropic API
┌──────────────────────┐   paper + question   ┌──────────────┐
│ Paperlens (this app) │ ───────────────────▶ │    Claude    │
│  key + library stay  │ ◀─────────────────── │              │
│  on your device      │   structured answer  └──────────────┘
└──────────────────────┘
```

There is **no Paperlens server**. The app is a single static page. When you analyse a paper, your browser sends it directly to the Anthropic API using **your own API key**, and the result is stored in your browser.

- **Your key** is saved only in your browser's local storage on that device. It is never written into any file in this repository.
- **Your papers** go to Anthropic and nowhere else.
- **Cost:** you pay Anthropic for your own usage. Long papers cost more, and chat re-sends the paper with each question (with caching turned on to keep follow-ups cheaper). Check your usage in the Anthropic console.

---

## Getting started

### 1. Get an API key
Create one at [console.anthropic.com](https://console.anthropic.com).

### 2. Open the app
Use the live address above, or [run it locally](#run-it-locally).

### 3. Add your key
Click the **gear icon**, paste your key, and save. Do this once per device.

### 4. Drop in a paper
Drag a PDF onto the page (up to about 24 MB and 100 pages), or paste text instead. Analysis takes roughly 30 to 90 seconds, and the overview appears as it's written.

No key yet? Click **See a finished example first** to try a sample paper with every feature.

---

## Install it as an app

Paperlens is a Progressive Web App, so it can live on your desktop or home screen with its own icon and window.

- **Chrome or Edge (desktop):** click the install icon in the address bar, or the **Install app** button in Paperlens.
- **Android (Chrome):** tap **Install app** from the menu.
- **iPhone or iPad (Safari):** tap **Share, then Add to Home Screen**.

Once installed, the app opens instantly and works offline for reading saved papers. Analysing a paper and chat need an internet connection.

---

## Deploy your own copy (GitHub Pages)

1. Create a **public** repository on GitHub (free Pages needs a public repo).
2. Upload everything in this folder: `index.html`, `sw.js`, `manifest.webmanifest`, and the icon files. On a new empty repo, use **uploading an existing file**. Otherwise use **Add file, then Upload files**.
3. Go to **Settings, then Pages**. Set the source to **Deploy from a branch**, branch **main**, folder **/ (root)**, and save.
4. After about a minute your app is live at `https://YOUR-USERNAME.github.io/REPO-NAME/`.

**Updating:** upload a new `index.html` with the same name and commit. GitHub can take a few minutes to publish it, then reload the app to see the change.

## Run it locally

Double-click `index.html` and it runs in your browser. For the full installable experience, serve it over HTTP:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

---

## Keyboard shortcuts

| Where | Keys |
|---|---|
| Flashcards | `Space` flip, `1` show again, `2` hard, `3` know it (or `←` / `→`) |
| Quiz blitz | `1` to `4` to answer |
| Fact or fiction | `T` / `F` (or `←` / `→`) |
| Chat | `Enter` send, `Shift+Enter` new line |
| Anywhere | `Esc` closes dialogs |

---

## Good to know

- **Check the important bits.** Summaries, figures and answers are written by AI. Page links are there so you can verify claims against the source, and you should for anything that matters.
- **Figure previews** are the real PDF pages rendered in your browser using [pdf.js](https://mozilla.github.io/pdf.js/), loaded from a CDN. They need an internet connection the first time.
- **Papers reopened from your library** don't keep the PDF (it's not stored), so page previews are unavailable until you attach the PDF again from the Figures or Chat tab.
- **Scanned PDFs** and very long documents may give weaker results than text-based PDFs.
- **Model:** the default is `claude-sonnet-5-5`. You can change it in Settings (for example to an Opus model for more depth, or Haiku for speed).

## Troubleshooting

| Problem | Try this |
|---|---|
| "The API key was rejected" | Open Settings and re-paste the key. Check it hasn't been revoked in the console. |
| "Could not reach api.anthropic.com" | Check your connection, and look for an ad blocker or privacy extension blocking the request. |
| "That model name was not found" | Open Settings and pick a valid model name. |
| "Rate limit reached" or "busy" | Wait a minute and try again. |
| PDF too large | Compress the PDF or split it. The limit is about 24 MB. |
| Figures show no page images | The PDF isn't attached (reopened from the library) or pdf.js couldn't load. Attach the PDF on the Figures tab. |
| No "Install app" button | Some browsers only offer install from a deployed address, not a local file. Safari uses Share, then Add to Home Screen. |

---

## What's in this folder

| File | Purpose |
|---|---|
| `index.html` | The whole app: interface, styles and logic in one file. |
| `sw.js` | Service worker: makes the app load instantly and work offline. It never touches the Anthropic API. |
| `manifest.webmanifest` | Tells browsers how to install the app (name, icons, colours). |
| `icon-*.png`, `apple-touch-icon.png`, `favicon-32.png`, `icon.svg` | App icons. |

To ship a change that must reach everyone immediately, edit `VERSION` at the top of `sw.js` so old cached copies are cleared.

---

## FAQ

**Does my paper get stored anywhere?** Only in your browser's saved library (as the generated notes, not the PDF) and with Anthropic when you analyse or chat. There is no other server.

**Can several people share one deployment?** Yes. Everyone opens the same address, but each person uses their own API key and has their own private library on their own device.

**Why do I need my own key?** Because there's no server to hold a shared one. Putting a key inside a public web page would expose it to everyone who visits, so Paperlens deliberately doesn't.

**Does it work offline?** The app opens and saved papers can be read. Analysis and chat need internet.
