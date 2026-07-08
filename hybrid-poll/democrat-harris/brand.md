# Democrat / Harris — reference build

The original hybrid-poll unit this repo is based on (kept intact as the reference).

- **`index.html`** — playable variant: interstitial start screen ("Watch & Vote"),
  tap-to-start reveals the video + poll.
- **`simple.html`** — direct variant: video autoplays muted (mute button), poll visible on load.
- **`democrat.mp4`** — the clip.

## Palette (dark theme)

| Var | Hex |
|---|---|
| `--accent` | `#3b82f6` |
| `--accent-light` | `#60a5fa` |
| `--bg` | `#0c1829` |
| `--bg-card` | `#132035` |
| `--text` | `#e8edf5` |

Font: DM Sans. Poll: "Rate Your Support", 1–5 agree/disagree scale.

> Note: these two files are the hand-written originals. The reusable, data-driven versions
> of this layout live in [`../_template/`](../_template/).
