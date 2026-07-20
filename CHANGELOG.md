# Changelog

Every release, newest first. The APK checksums live in each
[release](https://github.com/eVersor-HN/FindASet/releases) and in the [README](README.md).

---

## v1.10 — The deep-audit release · 2026-07-20

- **Logging got fast and stays fast.** Every food/weight entry used to rewrite its whole file on the spot, and each action re-scanned the entire history — after years of daily logs, every tap would have slowed down. Writes now happen in the background and each day is indexed; a tap costs the same on day 1 and day 1000.
- **A workout now survives its process being killed.** If Android reclaims the app mid-session (memory pressure, Doze), the session comes back — same phase, same tallies, paused and waiting. Re-entering a running workout resumes it instead of silently restarting it from zero.
- **The player's charge ring finally obeys your accent** — and the phase tints and colour-vision modes with it. It was the one surface still painted in its demo colours.
- **The notification and widget kcal bars are actually accent-coloured now** (they silently fell back to the system default on most launchers), and the widget shows your rest-day targets on rest days instead of the training goal.
- **Label scanner:** no more out-of-memory risk on 12 MP photos (a downsample bug decoded near full size), and it stops writing a diagnostic text file next to every scanned photo.
- **Boot sequence** replays on every app open — not once per day — and the report now sizes itself to the screen instead of scrolling.
- Honest touch targets (44 px controls grew invisible 48 dp hit areas), a scrollable confirm dialog for short landscape windows, weight trend arrows in two distinguishable colours, warnings in the warning colour, and the analysis screens stopped spraying the accent across every number.
- Smaller install: ~370 KB of spoken-line text moved out of compiled code into a lazily-loaded asset, and a dead animated component was removed.

## v1.9 — Landscape & colour vision · 2026-07-20

- **Landscape everywhere.** The app was locked to portrait; it rotates now.
- **Player:** the timer ring is centred properly and can no longer overflow a short window — that also fixed split-screen in portrait.
- **Calendar:** two panes in landscape, pick left / read right. Day grid capped in width, which also fixes oversized cells on tablets.
- **Launch screen:** report left, action rail right.
- **Label scanner:** framing guide derived from the window instead of a fixed height; controls move to a rail.
- **Fixed:** a photo taken after rotating was saved sideways and quietly ruined the OCR scan.
- **Colour vision:** deuteranopia, protanopia, tritanopia and monochrome modes. Alarm colours move to hues that survive the deficiency; statuses gain text markers so meaning never rests on colour alone.
- **Accent picker** draws each swatch as you actually see it and flags the ones that collide with the alarm colours — the default spring green is one of them under deuteranopia. One tap switches to the safest.
- **Fixed:** Android's "animator duration scale" setting silently disabled most animations — buttons never depressed, the hold-to-confirm bar filled instantly. The app now drives its own. (The 2-second hold gate itself was never affected.)
- Larger terminal type; the report scrolls with its own output. Ambient helix column beside it.
- Dropped the old start-up scanline — a 1.1s animation standing in front of a real boot sequence.

## v1.8 — Boot terminal · 2026-07-20

- **The app boots instead of opening.** A handshake that greets you by name, a self-test, the day's levels as ASCII gauges, what is scheduled, then the one action that matters.
- **The report knows the day.** Hard session, easy cardio, rest, already-trained — each gets its own levels, tone and alert block.
- **Self-test with a sense of humour:** `PAIN FILTER — OFFLINE`, `COMFORT ZONE — 404`. Dealt from a shuffled deck, so ~5 weeks pass before a line can repeat.
- **The start button glitches into place** — but only when something is actually pending. Rest days render it calm.
- **Operator name** under Settings; blank stays `UNREGISTERED`.
- Full sequence plays once a day, then the report is simply there. Tap to skip.
- **Green is spent, not sprayed.** Card frames and brackets were drawn in the accent unconditionally; chrome is neutral now, and the accent marks the primary gauge, the primary action and active states.
- Stats screens lost their green cast; the calendar marks only *selected* and *today*.
- Over-goal macros go properly red instead of a mild tint.
- **Attribution fix:** the two bundled fonts were shipping without a licence notice.

## v1.7 — Spring terminal · 2026-07-19

- App-wide re-skin from tactical HUD to a **phosphor terminal**: near-black ground, hard square edges, one monospaced typeface throughout.
- Spring green is the new default accent; all 16 accents still switch the whole app live.
- Green app icon.
- **Fixed:** angled corners had two independent sources, so some bars rendered with a mismatched outline.
- **Fixed:** a fresh install could start on the wrong accent.
- Dropped the unused legacy launcher icons (~300 KB).

## v1.6 — Tactical HUD · 2026-07-18

- App-wide **Tactical HUD** restyle, and before it the Fusion pass: OLED mono-accent, glowing frames, segment bars, dense macro table.
- **Automatic backups** on an interval and folder you choose.
- Back on the dashboard now asks before closing the app.
- Alert colour contrasts the selected accent, and only real alerts use it.
- Stripped the player's top header and the dashboard title.
- Hardening: obfuscated data layer, build fingerprints dropped.
- About card gained the author name and support links.

## v1.5 — Red default & 16 accents · 2026-07-13

- Cyberpunk-red default with **15 further selectable accents**, live across the whole app.
- Red dumbbell icon.
- App-wide elegance pass; rounder player controls and Add-Food buttons.

## v1.4 — Widget & modern cyberpunk · 2026-07-13

- **Home-screen widget:** today's kcal and P/C/F, tap to open.
- Modern-cyberpunk redesign — rounded, lighter type, quick-log dropdown.
- **Fixed:** voices overlapping; a line now fades when you leave a speaking screen.

## v1.3 — Compliance & food data · 2026-07-05

- First-run disclaimer gate, public-domain male voice, full third-party notices and About credits.
- FILL MACROS pinned below the scrolling log; camera-permission denial now explains itself.
- Food DB: cooked/skinless poultry variants, wing kcal fix, curated fill-pool preferences.

## v1.2 — One-tap flows · 2026-07-04

- One-tap session start on the home screen; wizard-first NEW, editor duplicate and name suggestions.
- Quick-log strip under the tanks; goals via the day banner.
- Weight: 0.1 kg steppers, per-day editing, delete confirm, clearable goal.
- Haptics on every control; CyberSwitch, CyberSlider and a date picker.

## v1.1 — Audit & hardening · 2026-07-04

- **Crash-safe persistence** and a hardened, transactional backup import.
- Correctness pass: per-day-type adherence, honest PRs, no double-logging.
- Strength / e1RM progression surfaced; responsive fixes.
- Food DB: corrected macros, peel-explicit names, whey, resilient loading, USDA name collisions fixed.
- Fill Macros: pin exact amounts per pool food.
- Rename foods anywhere; save without logging.
- One dialog / button / chip language everywhere; dropdowns start collapsed.

## v1.0 — First public release · 2026-06-30

The app as a whole: a fully offline training and nutrition companion.

- **Guided workout player** — timeline, circular timer, voice cues, spoken rest countdowns, hold-to-confirm.
- **Rep & set logging** with weight per set, e1RM tracking and spoken PR detection.
- **Neural offline voice** — sherpa-onnx + Piper, 20 cyberpunk personas, female and male, effects and equalizer.
- **Plans & calendar** — date-range plan blocks, weekly schedule, month/week logbook, per-day notes.
- **Macro tracking** — food library, favourites, quick log, training- vs rest-day goals, CSV export, analytics.
- **Offline label scanner** — on-device OCR with multi-column parsing, energy cross-check and preprocessing for hard labels.
- **FILL MACROS** — solves a food combination to hit the day's remaining macros.
- **Food database** — curated core plus USDA tail, searchable in 15 languages.
- **Body-weight tracking** with chart, trend and projection.
- Guided workout creator, drag-and-drop reordering, backup/restore, daily reminders.
- Release hardening: R8 obfuscation, release signing, proprietary EULA.
