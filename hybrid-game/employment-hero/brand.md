# Employment Hero — "Blow 'Em Away" hybrid game

Video on top (37%): the "Employment Operating System: Leap into the future of work" spot, re-encoded to
1280x720 (pillarbox cropped, H.264 CRF 27, faststart) = 3.5 MB — visually identical to the 1080p source at slot size.
Game below (63%): first-person leaf blower in Pete's office. Clear the apps before Pete's stress maxes out;
blast the Employment Hero orb (appears at 60% cleared) to pull every remaining app into one place.

- **Start:** "Tap to play" card (unlocks sound at 35% on every device). `?bot` = autopilot, `?sim` = 20 instant rounds.
- **Tuning:** everything in the `CONFIG` block (round length, badge growth, split, stress, heat, orb threshold).
- **Art:** office / app icons / bunny-arm blower generated in Gemini from greybox layout guides + film stills
  (pack + prompts kept locally in `_work/employment-hero-gemini-pack/`, not in this repo). Pete slider face is
  cropped from the generated office. Orb = real EH mark drawn in code.

## Brand
| Token | Hex | Source |
|---|---|---|
| `--purple` | `#B385FE` | EH app icon lilac |
| `--purple-deep` | `#2C0B3F` | EH app icon mark (aubergine) |

Logos: `assets/eh-logo-white.svg` (official wordmark, employmenthero.com), `eh-mark*.svg` (mark cropped from it).
CTA: Book a demo → https://employmenthero.com/demo/ (`window.clickTag` overrides).
