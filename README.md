# Hybrid Playable

Hybrid playable ad units — a **video on top + an interactive panel below**, in a single
self-contained HTML file (inline CSS/JS, one local video). Built to pitch mock creatives
to brands, parties and clients.

Each format lives in its own top-level folder. Today that's **`hybrid-poll/`** (video + poll).
Future formats (quiz, slider, etc.) become sibling folders alongside it.

```
hybrid-playable/
├── index.html            ← gallery: links every client mock
├── hybrid-poll/          ← FORMAT: video + poll
│   ├── _template/        ← copy these to start a new client
│   │   ├── index.html    ·  playable variant — interstitial "Watch & Vote" start gate
│   │   └── simple.html   ·  direct variant — video + poll both show on load (no gate)
│   ├── electoral-commission-nz/   ← client mock
│   │   ├── index.html
│   │   ├── video.mp4
│   │   └── brand.md
│   └── democrat-harris/           ← original reference build
│       ├── index.html    ·  playable variant
│       ├── simple.html   ·  direct variant
│       ├── democrat.mp4
│       └── brand.md
└── (future: hybrid-quiz/, hybrid-slider/, …)
```

## Golden rule — never overwrite a shipped version

Every client version stays intact forever. To make a change to something already sent out,
**copy the folder to a new name** (e.g. `electoral-commission-nz-v2/`) and edit the copy.
Never edit a folder that has already been shared.

## Make a new client mock in 3 steps

1. **Copy a template folder** into the format folder and rename it to the client
   (e.g. `hybrid-poll/acme/`). Pick `simple.html` (no start gate) or `index.html`
   (interstitial start gate) as your `index.html`.
2. **Drop the client's clip** into that folder and point `CONFIG.videoSrc` at it.
3. **Edit the two clearly-marked blocks** at the top of the file:
   - `EDIT ME ▸ THEME` — set `--accent` + the surface/text colours (all tints follow `--accent`).
   - `EDIT ME ▸ COPY & DATA` — the question, options, labels and fake result %s.

That's it — no build step. Open the HTML in a browser (or serve the folder) to preview.

> **Tip:** in `CONFIG.options`, wrap any label containing an apostrophe in `"double quotes"`
> (e.g. `"Yes, I'm all set!"`) so the apostrophe doesn't break the JS string.

## Preview locally

```bash
cd hybrid-poll
python -m http.server 8801
# open http://127.0.0.1:8801/electoral-commission-nz/index.html
```
