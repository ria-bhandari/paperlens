# Paperlens

**Understand any research paper in minutes.** Drop in a PDF and get a clear overview, the figures that matter, an interactive mind map, flashcards, three games, and a chat that answers questions about the paper. Works for any field.

### [Open Paperlens](https://ria-bhandari.github.io/paperlens/)

`https://ria-bhandari.github.io/paperlens/`

---

## What you get

| Tab | What it does |
|---|---|
| **Overview** | A TL;DR, a "worth a full read if…" line, a snapshot (study type, data, method, headline result), key findings with numbers, the problem and approach, a plain-English version, caveats, and a glossary. Each finding links to the PDF page it came from. |
| **Figures** | The figures, tables and diagrams that carry the paper. Each one is matched to its numbered caption in your PDF and cropped straight from the page, with what it shows, why it matters, a one-line takeaway, and a "Look closely" prompt for reading critically. Anything that can't be found in the PDF is set aside and clearly marked, never shown as a figure. |
| **Mind map** | An interactive map you can pan, zoom, expand and collapse. Click a node to read its note. Export as SVG or PNG for slides. |
| **Flashcards** | Flip cards with *Show again soon*, *Hard, later* and *I know this*. Filter by type (concepts, methods, results, terms, critique). Export to Anki. |
| **Play** | **Quiz blitz** (lives, a timer and streak bonuses), **Fact or fiction**, and **Pair up** (match terms to meanings against the clock). Questions you miss can be turned into flashcards in one click. |
| **Chat** | Ask anything about the paper. Answers are grounded in the full PDF, and page references open the page so you can check them. |
| **Library** | Every paper you analyze is saved on your own device, with your flashcard progress, best game scores and chat history. Search, sort, reopen where you left off, and export a backup. No account or login needed. |

Also: six themes (Paper, Spring, Golden hour, Fall, Winter, Dusk) with light and dark modes and an optional "follow the seasons" setting, Markdown notes export, and an "explain it for" setting (nearby-field researcher, specialist, or newcomer).

---

## Getting started

1. **Get an API key** at [console.anthropic.com](https://console.anthropic.com).
2. **[Open Paperlens](https://ria-bhandari.github.io/paperlens/).**
3. **Add your key.** Click the gear icon, paste the key, and save. Do this once per device.
4. **Drop in a paper.** Drag a PDF onto the page (up to about 24 MB and 100 pages), or paste the text instead. Analysis takes roughly 30 to 90 seconds, and the overview appears as it's written.

No key yet? Click **See a finished example first** to try a sample paper with every feature.

---

## Install it as an app

Paperlens can live on your desktop or home screen with its own icon and window.

- **Chrome or Edge (desktop):** click the install icon in the address bar, or the **Install app** button in Paperlens.
- **Android (Chrome):** tap **Install app** from the menu.
- **iPhone or iPad (Safari):** tap **Share, then Add to Home Screen**.

Once installed, the app opens instantly and works offline for reading saved papers. Analysing a paper and chat need an internet connection.

---

## Your privacy and your key

There is **no Paperlens server**. When you analyse a paper or ask a question, your browser sends it directly to the Anthropic API using **your own API key**.

- **Your key** is saved only in your browser on that device. It is never sent anywhere except to Anthropic.
- **Your papers** go to Anthropic and nowhere else.
- **Your library** (the generated notes, your progress and, unless you switch it off in Settings, a copy of each PDF) is stored in your browser on your own device. It is never uploaded anywhere, which is also why no account is needed. Use **Library, then Export backup** to keep a copy or move to another device.
- **Cost:** you pay Anthropic for your own usage. Long papers cost more, and chat re-sends the paper with each question (with caching turned on to keep follow-ups cheaper). Check your usage in the Anthropic console.

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
- **Figure previews** are the real PDF pages rendered in your browser. They need an internet connection the first time.
- **Your library is per browser and per device.** A different browser, a private window, or cleared browsing data means a fresh, empty library, and some browsers clear data for sites you rarely visit. Installing Paperlens as an app and exporting a backup now and then keeps your papers safe.
- **Scanned PDFs** and very long documents may give weaker results than text-based PDFs.
- **Model:** the default is `claude-sonnet-5-5`. You can change it in Settings (for example to an Opus model for more depth, or Haiku for speed).

## Troubleshooting

| Problem | Try this |
|---|---|
| "The API key was rejected" | Open Settings and re-paste the key. Check it hasn't been revoked in the console. |
| "Could not reach api.anthropic.com" | Check your connection, and look for an ad blocker or privacy extension blocking the request. |
| "Your key isn't tied to a workspace" | In the Anthropic console, create a key inside a named workspace, or paste that workspace's ID (starts with `wrkspc_`) into the Workspace ID box in Settings. |
| "That model name was not found" | Open Settings and pick a valid model name. |
| My papers disappeared | The library lives in one browser on one device. Check you're in the same browser and not a private window, or use Library, then Import backup. |
| "Rate limit reached" or "busy" | Wait a minute and try again. |
| PDF too large | Compress the PDF or split it. The limit is about 24 MB. |
| Figures show no images | The saved PDF was removed (or "Keep a copy" is off in Settings), or the figure is a scan with no text caption. Attach the PDF on the Figures tab. Items listed under "Couldn't match" weren't found as numbered figures or tables in the PDF. |
| No "Install app" button | Not every browser offers it. On iPhone or iPad use Share, then Add to Home Screen. |

---

## FAQ

**Does my paper get stored anywhere?** Only on your own device (the notes, and a copy of the PDF if "Keep a copy" is on in Settings), and with Anthropic when you analyze or chat. There is no other server. You can delete any paper, or just its saved PDF, from the Library.

**Can anyone use it?** Yes, just open the link above. Each person uses their own API key and has their own private library on their own device, with no login.

**Why do I need my own key?** There's no server to hold a shared one, and a key placed inside a public web page would be exposed to every visitor, so Paperlens deliberately doesn't do that.

**Does it work offline?** The app opens and saved papers can be read. Analysis and chat need internet.

---

© 2026 Ria Bhandari. All rights reserved. The source in this repository is published only so the app can be hosted at the link above. Copying, redistributing or deploying your own copy is not permitted without permission.
