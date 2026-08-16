# FindASet

**FindASet** is an offline-first Android **training & nutrition companion**. It builds and runs
your workouts with a neural voice announcer, counts reps, tracks weight-per-set and PRs, logs
your macros and body-weight, and reads nutrition labels with an on-device scanner — everything
lives **on your phone**. No account, no cloud, no ads, no tracking; the one feature that can
reach the internet is an **optional, off-by-default barcode lookup** you switch on yourself.

> **Closed-source, proprietary application.** Free to use (including commercially) —
> **not for sale, not redistributable, not modifiable, no reverse-engineering.**
> See [LICENSE](LICENSE) and [DISCLAIMER](DISCLAIMER.md).

> 💸 Every rep you logged here was paid for with someone else's unpaid evenings, and your
> contribution to that total is a personal best in the wrong direction.
> **Ko-fi:** [ko-fi.com/eversorhn](https://ko-fi.com/eversorhn)
> **PayPal:** paypal.me/FAMarco
> **Bitcoin:** `bc1qv92c3eyeqvhgfnez7spfd7v2aytkhpshsl65yv`

Author / copyright: **© 2026 Marco Aurelio Fattizzo** ([@eVersor-HN](https://github.com/eVersor-HN)).
This is the **official** distribution repository — get FindASet only from here:
**https://github.com/eVersor-HN/FindASet**

---

## Download & install

1. Open the [**Releases**](https://github.com/eVersor-HN/FindASet/releases) page and download
   the latest **`FindASet-<version>.apk`**.
2. **Verify it is the genuine original** (see below) before installing it.
3. On your phone, open the APK and allow installing from this source if prompted
   ("Install unknown apps"). Follow the installer. FindASet is sideloaded — it is **not** on
   the Play Store.

There is nothing else to install — the app ships with everything it needs (voice models,
food database, label-scanner OCR) and downloads nothing on its own. The only network request it
can ever make is the optional barcode lookup, and only after you turn it on.

---

## ✅ Verify authenticity (SHA-256)

Every official release publishes the **SHA-256 checksum** of the APK. Comparing the checksum of
your download against the published value proves the file is the **unmodified original** and was
not tampered with. (The same repository address and this verification hint are shown inside the
app under **Settings → About**.)

**v1.17 — `FindASet-1.17.apk`:**

```
158816b958c0c5eab6c1c199a5230cc18fa73164aaabf3a12614db3b4d4d9023
```

The authoritative value for each release is in that release's notes and in its
[`SHA256SUMS.txt`](SHA256SUMS.txt) asset.

**Check it:**

```powershell
# Windows (PowerShell)
Get-FileHash .\FindASet-1.17.apk -Algorithm SHA256
```

```bash
# macOS                            # Linux
shasum -a 256 FindASet-1.17.apk    sha256sum FindASet-1.17.apk
```

The printed hash must match the value above (case-insensitive). If it does **not** match, do
**not** install the file — it is not the genuine FindASet build. The APK is signed with the
author's release key (`CN=Marco Aurelio Fattizzo, O=FindASet, C=DE`); Android will refuse any
later update that is not signed with the same key.

---

## Features

- **Boot terminal** — the app opens on a status report rather than a menu: a self-test, the day's
  subsystem levels, what is scheduled and a direct start. It reads today's plan, so a rest day, an
  easy day and a hard day each get their own readout.
- **Guided workout builder** — a simple, step-by-step wizard walks you from a name through your
  exercise list to timing and schedule, with the estimated total workout duration shown as you build.
- **Guided workout player** — timeline, circular timer, voice cues, spoken rest countdowns and
  periodic time call-outs.
- **Rep & set logging** — optional auto-tempo and count-aloud, weight per set, estimated 1RM
  tracking, PR detection announced by the voice.
- **Plans & calendar** — weekly training plans, month/week logbook, heatmap, streaks,
  per-day notes. Call a single day off from the dashboard and its macro targets, reminder and
  readouts switch to rest without touching the plan; press again to put it back.
- **Macro tracking** — quick-log dropdown, food library with favourites, fuel-tank goals, a
  multilingual food database (15 languages) and a **FILL MACROS** calculator that solves food
  amounts to hit the day's remaining macros.
- **Multilingual label scanner** — on-device OCR reads kcal / protein / carbs / fat from a
  photographed nutrition label across many languages, tells calories from kilojoules, and runs an
  energy cross-check that repairs gaps. Optionally switch on a barcode lookup to fetch exact values
  online when a label is unreadable. *(Always verify scanned values.)*
- **Neural offline voice** — an on-device announcer (female & male) with selectable styles,
  personas and effects. Rendered entirely on-device.
- **Body-weight tracking** — daily log with 0.1 kg steppers, goal line and trend.
- **Home-screen widget** — today's calories and protein / carbs / fat at a glance; tap to open.
- **Colour-vision support** — deuteranopia, protanopia, tritanopia and monochrome modes. The alarm
  colours move to hues that survive the deficiency, statuses gain text markers so meaning never
  rests on colour alone, and the accent picker shows each swatch as you actually see it.
- **Portrait and landscape** — every screen lays itself out for the orientation it is in; the
  player, calendar and label scanner switch to side-by-side arrangements rather than squeezing.
- **No account, no cloud, no ads, no tracking** — your data stays on the device, with local
  backup export/import built in. The one network feature — the optional barcode lookup — is off
  until you enable it, and even then only a scanned barcode number is sent.

## System requirements

- **Android 8.0 (API 26)** or newer, **arm64-v8a** device.
- ~95 MB free space for the APK (voice models, food database and scanner models included).

## License (summary)

FindASet is **proprietary, closed-source** software under the **FindASet EULA**
(full text in [`LICENSE`](LICENSE)):

- ✅ **Use** it for any purpose, **including commercially** (companies may use it internally).
- ✅ It is **free of charge**. To share it, point people to this repository.
- ❌ **No redistributing or passing on copies**, **no selling**, **no modifying / adapting**,
  **no reverse-engineering, decompiling or disassembling** — except where a bundled third-party
  license or mandatory law (e.g. § 69e UrhG) provides otherwise.

It bundles third-party components under their own licenses — AndroidX / Jetpack Compose, Kotlin,
kotlinx.serialization, CameraX (Apache-2.0), ML Kit Text Recognition & Barcode Scanning (ML Kit
ToS, on-device models), the neural-TTS stack **sherpa-onnx** (Apache-2.0) / **ONNX Runtime** (MIT) / **Piper** &
**piper-phonemize** (MIT) / **eSpeak NG** (GPL-3.0, remains under its own license), the Piper
voice models *kristin* & *john* (public-domain LibriVox recordings) and food data derived from
**USDA FoodData Central** (public domain). Full details and license texts:
[`THIRD_PARTY_NOTICES.md`](THIRD_PARTY_NOTICES.md).

No warranty — FindASet is a personal bookkeeping tool, **not medical, dietary, or fitness
advice**; figures (including scanned label values) are estimates. Exercise carries risk — train
within your limits. See [`DISCLAIMER.md`](DISCLAIMER.md).
