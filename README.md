# FindASet

**FindASet** is a fully offline Android **training & nutrition companion**. It builds and runs
your workouts with a neural voice announcer, counts reps, tracks weight-per-set and PRs, logs
your macros and body-weight, and reads nutrition labels with an on-device scanner — all **on
your phone, with no internet access at all** (the app declares no `INTERNET` permission and
contains no networking code).

> **Closed-source, proprietary application.** Free to use (including commercially) —
> **not for sale, not redistributable, not modifiable, no reverse-engineering.**
> See [LICENSE](LICENSE) and [DISCLAIMER](DISCLAIMER.md).

> 💛 **FAS is free.** If it makes your training better, you can support development with a
> donation: **PayPal [paypal.me/FAMarco](https://paypal.me/FAMarco)** (`@FAMarco`). Thank you!

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
food database, label-scanner OCR) and never downloads anything.

---

## ✅ Verify authenticity (SHA-256)

Every official release publishes the **SHA-256 checksum** of the APK. Comparing the checksum of
your download against the published value proves the file is the **unmodified original** and was
not tampered with. (The same repository address and this verification hint are shown inside the
app under **Settings → About**.)

**v1.3 — `FindASet-1.3.apk`:**

```
99618ced414dfc8ed6564d7dec14c0be3a93924d9994210beddee01a5fb3b243
```

The authoritative value for each release is in that release's notes and in its
[`SHA256SUMS.txt`](SHA256SUMS.txt) asset.

**Check it:**

```powershell
# Windows (PowerShell)
Get-FileHash .\FindASet-1.3.apk -Algorithm SHA256
```

```bash
# macOS                          # Linux
shasum -a 256 FindASet-1.3.apk   sha256sum FindASet-1.3.apk
```

The printed hash must match the value above (case-insensitive). If it does **not** match, do
**not** install the file — it is not the genuine FindASet build. The APK is signed with the
author's release key (`CN=Marco Aurelio Fattizzo, O=FindASet, C=DE`); Android will refuse any
later update that is not signed with the same key.

---

## Features

- **Guided workout player** — timeline, circular timer, voice cues, spoken rest countdowns and
  periodic time call-outs.
- **Rep & set logging** — optional auto-tempo and count-aloud, weight per set, estimated 1RM
  tracking, PR detection announced by the voice.
- **Plans & calendar** — weekly training plans, month/week logbook, heatmap, streaks,
  per-day notes.
- **Macro tracking** — quick-log strip, food library with favourites, fuel-tank goals, a
  multilingual food database (15 languages) and a **FILL MACROS** calculator that solves food
  amounts to hit the day's remaining macros.
- **Offline label scanner** — on-device OCR reads kcal / protein / carbs / fat from a
  photographed nutrition label, with image pre-processing for hard labels and an energy
  cross-check that repairs gaps. *(Always verify scanned values.)*
- **Neural offline voice** — an on-device announcer (female & male) with selectable styles,
  personas and effects. Fully offline, like everything else.
- **Body-weight tracking** — daily log with 0.1 kg steppers, goal line and trend.
- **No account, no cloud, no ads, no tracking** — your data never leaves the device; local
  backup export/import built in.

## System requirements

- **Android 8.0 (API 26)** or newer, **arm64-v8a** device.
- ~90 MB free space for the APK (voice models and food database included).

## License (summary)

FindASet is **proprietary, closed-source** software under the **FindASet EULA**
(full text in [`LICENSE`](LICENSE)):

- ✅ **Use** it for any purpose, **including commercially** (companies may use it internally).
- ✅ It is **free of charge**. To share it, point people to this repository.
- ❌ **No redistributing or passing on copies**, **no selling**, **no modifying / adapting**,
  **no reverse-engineering, decompiling or disassembling** — except where a bundled third-party
  license or mandatory law (e.g. § 69e UrhG) provides otherwise.

It bundles third-party components under their own licenses — AndroidX / Jetpack Compose, Kotlin,
kotlinx.serialization, CameraX (Apache-2.0), ML Kit Text Recognition (ML Kit ToS, on-device
model), the neural-TTS stack **sherpa-onnx** (Apache-2.0) / **ONNX Runtime** (MIT) / **Piper** &
**piper-phonemize** (MIT) / **eSpeak NG** (GPL-3.0, remains under its own license), the Piper
voice models *kristin* & *john* (public-domain LibriVox recordings) and food data derived from
**USDA FoodData Central** (public domain). Full details and license texts:
[`THIRD_PARTY_NOTICES.md`](THIRD_PARTY_NOTICES.md).

No warranty — FindASet is a personal bookkeeping tool, **not medical, dietary, or fitness
advice**; figures (including scanned label values) are estimates. Exercise carries risk — train
within your limits. See [`DISCLAIMER.md`](DISCLAIMER.md).
