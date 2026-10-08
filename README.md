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
| **Library** | Every paper you analyze is saved on your own device, with your flashcard progress, best game scores and chat history. Sort papers into **folders** by discipline or project (drag and drop, or one tap), star them, mark them To read / Reading / Read, and search across titles, summaries, findings and your own notes. No account or login needed. |
| **Notes** | A private notepad for each paper, saved as you type, with a place for "relevance to my research" and themes. Drop findings and chat answers straight in with **＋ note** and **Save to notes**. |
| **Cite** | On every Overview: APA, BibTeX and RIS (imports into Zotero, Mendeley and EndNote). Details are editable, and a DOI is only included if it is printed in the paper itself. |
| **Compare** | Select 2 to 8 papers and get a literature-review matrix: aim, method, findings and limitations side by side, oldest first, plus your own "relevance" and "theme" columns. Export to Excel (CSV), Markdown or BibTeX. |

Equations are typeset like LaTeX, so $e^{x}$ shows as a proper formula. Also: six themes (Paper, Spring, Golden hour, Fall, Winter, Dusk) with light and dark modes and an optional "follow the seasons" setting, Markdown notes export, and an "explain it for" setting (nearby-field researcher, specialist, or newcomer).

---

## Getting started

1. **Get an API key** from an AI service ([Anthropic](https://console.anthropic.com) is the recommended default, and [OpenRouter](https://openrouter.ai/keys) is the easiest way to use other models). See [Choose your AI service](#choose-your-ai-service).
2. **[Open Paperlens](https://ria-bhandari.github.io/paperlens/).**
3. **Add your key.** Click the gear icon, paste the key, and save. Do this once per device.
4. **Drop in a paper.** Drag a PDF onto the page (up to about 24 MB and 100 pages), or paste the text instead. Analysis takes roughly 30 to 90 seconds, and the overview appears as it's written.

No key yet? Click **See a finished example first** to try a sample paper with every feature.

---

## Choose your AI service

Open **Settings** (the gear icon), pick a service, paste its key, and press **Test connection**. Each service keeps its own key, so you can switch freely.

| Service | Get a key | How it reads the paper | Works from a web page? |
|---|---|---|---|
| **Anthropic (Claude)** | [console.anthropic.com](https://console.anthropic.com) | Reads the PDF directly, figures included | Yes |
| **OpenRouter** | [openrouter.ai/keys](https://openrouter.ai/keys) | Text extracted in your browser | Yes. One key reaches Claude, GPT, Gemini, Llama and many more |
| **OpenAI** | [platform.openai.com/api-keys](https://platform.openai.com/api-keys) | Reads the PDF directly | Often blocked by OpenAI (CORS). Use OpenRouter for OpenAI models, or enter a proxy address |
| **Google Gemini** | [aistudio.google.com/apikey](https://aistudio.google.com/apikey) | Text extracted in your browser | Use **Test connection** to check |
| **Other (OpenAI-compatible)** | Your service | Text extracted in your browser | Depends on the service. Local servers (Ollama, LM Studio) work if they allow browser access |

Anthropic is the most thoroughly tested option. The others use the standard OpenAI-style chat format, but every service names its models differently and changes them often, so always check the exact model name on the service's own site.

## Install it as an app

Paperlens can live on your desktop or home screen with its own icon and window.

- **Chrome or Edge (desktop):** click the install icon in the address bar, or the **Install app** button in Paperlens.
- **Android (Chrome):** tap **Install app** from the menu.
- **iPhone or iPad (Safari):** tap **Share, then Add to Home Screen**.

Once installed, the app opens instantly and works offline for reading saved papers. Analysing a paper and chat need an internet connection.

---

## Your privacy and your key

There is **no Paperlens server**. When you analyse a paper or ask a question, your browser sends it directly to the AI service you choose (Anthropic by default) using **your own API key**.

- **Your key** is saved only in your browser on that device. It is never sent anywhere except to the service you chose.
- **Your papers** go to the AI service you choose and nowhere else.
- **Your library** (the generated notes, your progress and, unless you switch it off in Settings, a copy of each PDF) is stored in your browser on your own device. It is never uploaded anywhere, which is also why no account is needed. Use **Library, then Export backup** to keep a copy or move to another device.
- **Cost:** you pay your chosen AI service for your own usage. Long papers cost more, and chat re-sends the paper with each question (with caching turned on to keep follow-ups cheaper). Check your usage on that service's website.

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
- **Equations** are written by the AI in LaTeX and drawn with [KaTeX](https://katex.org). KaTeX loads from the internet the first time (then it is remembered); until it loads, or offline, formulas show as readable text such as eˣ. Services that read your paper as extracted text (OpenRouter, Gemini and others) see equations as they come out of the PDF, which can be scrambled, so Anthropic and OpenAI are better for maths-heavy papers.
- **Folders, notes and statuses** are stored with your library on this device, and are included in **Export backup**. Deleting a folder never deletes its papers.
- **Your library is per browser and per device.** A different browser, a private window, or cleared browsing data means a fresh, empty library, and some browsers clear data for sites you rarely visit. Installing Paperlens as an app and exporting a backup now and then keeps your papers safe.
- **Scanned PDFs** and very long documents may give weaker results than text-based PDFs.
- **Model:** the default for Anthropic is `claude-sonnet-5-5`. You can change the model in Settings (for example Opus for more depth, or Haiku for speed). Model names change often, so use **Test connection** to check one works.
- **Which service reads the paper best?** Anthropic and OpenAI read the PDF directly, including its figures. Other services (OpenRouter, Gemini, and others) are sent the paper's text, extracted in your browser, so they describe figures from their captions and surrounding text, and a scanned PDF with no selectable text won't work with them.

## Troubleshooting

| Problem | Try this |
|---|---|
| "…rejected the API key" | Open Settings, make sure the right AI service is selected, and re-paste that service's key. Check it hasn't been revoked. |
| "Could not reach …" | Check your connection, and look for an ad blocker or privacy extension. If it names a service other than Anthropic or OpenRouter, that service may not allow requests from web pages (a browser rule called CORS). OpenAI often blocks them: use OpenRouter instead, or enter a proxy address in Settings. |
| "Your key isn't tied to a workspace" | In the Anthropic console, create a key inside a named workspace, or paste that workspace's ID (starts with `wrkspc_`) into the Workspace ID box in Settings. |
| "…could not find that model" | Open Settings, copy the exact model name from the service's own model list, and press **Test connection**. |
| A formula shows as plain text | KaTeX hasn't loaded (offline or blocked). Readable text such as eˣ is shown instead, and the real formula appears once it loads. |
| My papers disappeared | The library lives in one browser on one device. Check you're in the same browser and not a private window, or use Library, then Import backup. |
| "Rate limit reached" or "busy" | Wait a minute and try again. |
| PDF too large | Compress the PDF or split it. The limit is about 24 MB. |
| Figures show no images | The saved PDF was removed (or "Keep a copy" is off in Settings), or the figure is a scan with no text caption. Attach the PDF on the Figures tab. Items listed under "Couldn't match" weren't found as numbered figures or tables in the PDF. |
| No "Install app" button | Not every browser offers it. On iPhone or iPad use Share, then Add to Home Screen. |

---

## FAQ

**Does my paper get stored anywhere?** Only on your own device (the notes, and a copy of the PDF if "Keep a copy" is on in Settings), and with the AI service you chose when you analyze or chat. There is no other server. You can delete any paper, or just its saved PDF, from the Library.

**Can anyone use it?** Yes, just open the link above. Each person uses their own API key and has their own private library on their own device, with no login.

**Why do I need my own key?** There's no server to hold a shared one, and a key placed inside a public web page would be exposed to every visitor, so Paperlens deliberately doesn't do that.

**Does it work offline?** The app opens and saved papers can be read. Analysis and chat need internet.

---

© 2026 Ria Bhandari. All rights reserved. The source in this repository is published only so the app can be hosted at the link above. Copying, redistributing or deploying your own copy is not permitted without permission.
