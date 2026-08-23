# FindASet

**Local training and nutrition control. No account. No cloud. No observers.**

FindASet runs your training and your fuel from a single system on the device in your hand.
It builds and drives workouts with a neural announcer, counts reps and load, tracks personal
records, logs macros and body-weight, and reads nutrition labels straight off the packaging —
without a login, a subscription, or a server that has to be reachable for the app to work.

Built for people who train with intent and expect their record to stay theirs.

---

## Product status

**Closed-source, proprietary software.**
© 2026 **Marco Aurelio Fattizzo** ([@eVersor-HN](https://github.com/eVersor-HN)).

Free of charge for any purpose, including commercial use. **Not for sale, not
redistributable, not modifiable, no reverse-engineering.** The authoritative terms are in
[`LICENSE`](LICENSE); liability and scope are set out in [`DISCLAIMER.md`](DISCLAIMER.md).

---

## Support the project

> **Ko-fi:** https://ko-fi.com/eversorhn
> **PayPal:** https://paypal.me/FAMarco (`@FAMarco`)
> **Bitcoin:** `bc1qv92c3eyeqvhgfnez7spfd7v2aytkhpshsl65yv`

> 💸 *You extracted joy and gave nothing back.
> History's worst people started exactly this small.*

---

## Local first // private by design

- **No account.** No sign-up, no profile, no login, no server-side identity.
- **No telemetry, no analytics, no ads, no tracking.**
- **Your data stays on the device.** Training log, macros, body-weight, food library and
  settings live in the app's private storage. Backup export and import are local and manual.
- **Ships complete.** Voice, food database and label scanner are on the device from the first
  launch. The app fetches nothing on its own.
- **One network feature, and it is off by default:** the optional barcode lookup. Enable it and
  a scanned barcode number is sent to **Open Food Facts** to retrieve that product's nutrition
  values. Leave it off and FindASet makes no network requests at all.
- **Permissions:** camera (label and barcode scanning) and notifications (live macro and
  workout status, reminders). Nothing further.

---

## Official distribution

Author: **eVersor-HN** — Marco Aurelio Fattizzo
Official repository: **https://github.com/eVersor-HN/FindASet**

This repository is the sole official source. Builds are published only on its
[**Releases**](https://github.com/eVersor-HN/FindASet/releases) page. FindASet is not on the
Play Store or any other app store — any copy obtained elsewhere is unofficial, unverified and
unsupported.

---

## Download & install

1. Download the latest **`FindASet-<version>.apk`** from the
   [Releases](https://github.com/eVersor-HN/FindASet/releases) page.
2. **Verify the SHA-256** against the value published with that release (see below).
3. Open the APK on the device and allow installation from this source when prompted
   ("Install unknown apps"), then follow the installer.
4. Nothing to configure — the app is operational on first launch.

---

## Verify authenticity // SHA-256

Every official binary is published with its **SHA-256 checksum** in the corresponding GitHub
Release. Filename and hash must match exactly; a match proves the file is the unmodified
original. The same repository address and this verification hint are shown in the app under
**Settings → About**.

**v1.18 — `FindASet-1.18.apk`:**

```
2044a316924e5698c402c315b53886b621e4695288c28de171013ce47838cda9
```

```powershell
# Windows (PowerShell)
Get-FileHash .\FindASet-1.18.apk -Algorithm SHA256
```

```bash
# macOS                            # Linux
shasum -a 256 FindASet-1.18.apk    sha256sum FindASet-1.18.apk
```

If the printed hash does **not** match, do **not** install the file — it is not the genuine
FindASet build. The authoritative value for each release is in that release and in
[`SHA256SUMS.txt`](SHA256SUMS.txt). Builds are signed with the author's release key
(`CN=Marco Aurelio Fattizzo, O=FindASet, C=DE`); Android refuses any update not signed with
the same key.

---

## Features

**CONTROL**
- Operates locally. No account, no cloud dependency, no subscription.
- Your plan, your log, your food library — exported and restored on your terms.
- Sixteen selectable interface accents; the whole app follows the one you pick.

**TRAINING**
- **Boot report** — the app opens on a status readout rather than a menu: self-test, the day's
  subsystem levels, what is scheduled, and a direct start. Rest day, easy day and hard day each
  get their own readout.
- **Guided builder** — a step-by-step flow from name through exercises to timing and schedule,
  with the estimated session duration updating as you build.
- **Guided player** — timeline, circular timer, voice cues, spoken rest countdowns, periodic
  time call-outs and a tempo bar that opens and closes at the exercise's own rhythm.
- **Rep and set logging** — optional auto-tempo and count-aloud, weight per set, estimated 1RM
  tracking, personal records detected and announced.
- **Live session overview** — everything done with its result, what is running, what is still
  coming, and on-the-spot corrections to both logged and upcoming sets.
- **Plans and calendar** — weekly plans, month and week logbook, heatmap, streaks, per-day
  notes. Stand a single day down and its macro targets, reminder and readouts switch to rest
  without touching the plan.
- **Session report** — a finished workout writes itself up as a shareable report; the newest
  twenty are kept and managed from the settings.

**NUTRITION**
- **Macro tracking** — quick-log dropdown, food library with favourites, fuel-tank goals, and
  separate targets for training and rest days.
- **FILL MACROS** — a calculator that solves food amounts to hit the day's remaining macros.
- **Multilingual food database** — searchable in 15 languages.
- **Label scanner** — reads kcal, protein, carbs and fat from a photographed nutrition label
  across many languages, tells calories from kilojoules, and cross-checks the energy figure to
  repair gaps. An optional barcode lookup can fetch exact values when a label is unreadable.
- **Body-weight tracking** — daily log with 0.1 kg steppers, goal line and trend.
- **Reset on demand** — clear a single day or the entire logged history, each behind its own
  confirmation. Goals and favourites are never touched.

**VOICE**
- **Neural offline announcer** — female and male, with selectable styles, personas and effects.
  Rendered entirely on the device, and released from memory when it is not in use.

**INTERFACE**
- **Home-screen widget** — today's calories and protein / carbs / fat at a glance; tap to open.
- **Colour-vision modes** — deuteranopia, protanopia, tritanopia and monochrome. Alert colours
  move to hues that survive the deficiency, statuses gain text markers so meaning never rests
  on colour alone, and each accent swatch is shown as you actually see it.
- **Portrait and landscape** — every screen lays itself out for the orientation it is in.

---

## Limitations // security // privacy

- **Scanned values are estimates.** Always verify what the label scanner or the barcode lookup
  returns before you rely on it.
- **The barcode lookup leaves the device.** It is off until you enable it; when enabled, the
  scanned barcode number is sent to Open Food Facts. No other data is transmitted.
- **No cloud sync.** Data exists only on the device it was entered on. Uninstalling the app
  removes it — use the built-in backup export to keep a copy.
- **Sideloaded distribution.** Updates are manual: download and verify each new release
  yourself. There is no automatic update channel.
- **Not medical, dietary or fitness advice.** FindASet is a personal bookkeeping tool; all
  figures are estimates. Exercise carries risk — train within your limits. See
  [`DISCLAIMER.md`](DISCLAIMER.md).

---

## System requirements

- **Android 8.0** or newer
- **arm64-v8a** device
- **~95 MB** free storage (voice, food database and scanner assets included)
- Camera required for label and barcode scanning

---

## License

FindASet is **proprietary, closed-source** software licensed under the **FindASet EULA** —
full text in [`LICENSE`](LICENSE):

- ✅ **Use** it for any purpose, **including commercially**.
- ✅ It is **free of charge**. To share it, point people to this repository.
- ❌ **No redistribution**, **no resale**, **no modification or adaptation**, **no reverse
  engineering, decompilation or disassembly** — except where a bundled third-party license or
  mandatory law (e.g. § 69e UrhG) provides otherwise.

Ownership of the software remains with the copyright holder. You receive a limited right to use
the distributed application, nothing more.

## Third-party notices

FindASet bundles third-party components that remain governed by their own licenses, including
components under Apache-2.0, MIT, GPL-3.0, the SIL Open Font License and vendor terms, plus
public-domain voice and food data. Full attribution and license texts:
[`THIRD_PARTY_NOTICES.md`](THIRD_PARTY_NOTICES.md).
