# Guzman y Gomez (US) — brand kit

Mock hybrid-CTA unit for the GYG app-download offer: **new users get a free regular burrito
(valued up to $14.50) on downloading the app and signing up to GOMEX Rewards.**

- **Format:** `hybrid-cta` — video on top (37%), branded CTA panel below (63%). No start gate.
- **Video:** `video.mp4` — GYG "ALL IN" 30s spot (16:9, 1280×720).
- **Interaction:** tap the GOMEX voucher → "CLAIMED!" stamp slams on, CTA flips to
  "DOWNLOAD TO REDEEM" and pulses. CTA / badges click out (iOS → App Store, else Google Play;
  `window.clickTag` overrides). Store URLs in `CONFIG` are search placeholders — swap for real listings.

## Fonts (from guzmanygomez.com theme CSS, files in `fonts/`)

| Face | File | Used as |
|---|---|---|
| Sinibold | `sini-bold-webfont-webfont.woff2` | Headline, sub-line, voucher item, CTA button, CLAIMED stamp (`--f-display`) |
| Guzman Bold Caps | `guzman_bold_caps-webfont.woff2` | "GOMEX" and "FREE" on the voucher (`--f-brand`). The webfont lacks proper caps I, V, Y — keep it to words without them |
| Montserrat | Google Fonts | Body, value line, T&Cs (`--f-body`) |

## Palette

| Token | Hex | Source / use |
|---|---|---|
| `--yellow` | `#FFD204` | GYG gold — panel background |
| `--cream` | `#FFECA9` | Logo sunburst rays — rotating background rays |
| `--ink` | `#171717` | Site black — type, CTA button, badges |
| `--ink-soft` | `#231F20` | Logo black (reference) |
| `--paper` | `#FFF9E5` | Site light cream — voucher stock |
| `--chilli` | `#D70015` | Site red — "CLAIMED!" stamp |

Layout follows the "FREE BURRITO / DOWNLOAD OUR NEW APP AND SIGN UP TO GOMEX!" poster:
black condensed headline on gold, store badges + @guzmanygomezus bottom-left, logo bottom-right.
