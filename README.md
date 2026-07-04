<div align="center">
  <img src="LOGO-FAS.png" alt="FindASet" width="160">

  # FindASet

  **A fully offline Android training & nutrition companion.**
  Closed-source · no account · no cloud · no tracking.

  Copyright © 2026 **Marco Aurelio Fattizzo** · All rights reserved.
</div>

---

FindASet builds and runs your workouts with a voice announcer, counts reps, tracks
weight-per-set and PRs, logs your macros and body-weight, and reads nutrition
labels with an on-device scanner — all **on your phone, with no internet access at
all**. The app declares **no `INTERNET` permission** and contains no networking
code; everything stays in the app's private storage.

> This is the **official release repository** — the only authentic source of the
> app. The source code is **not public** (FindASet is closed source).

## Features

- **Guided workout player** — timeline, circular timer, voice cues, spoken rest
  countdowns and periodic time call-outs.
- **Rep & set logging** — optional auto-tempo and count-aloud, weight per set,
  estimated 1RM tracking, PR detection announced by the voice.
- **Plans & calendar** — weekly training plans, month/week logbook, heatmap,
  streaks, per-day notes.
- **Macro tracking** — quick-log strip, food library, favourites, fuel-tank goals,
  a multilingual food database and a macro "fill" calculator.
- **Offline label scanner** — on-device OCR reads kcal / protein / carbs / fat from
  a photographed nutrition label, with image pre-processing for hard labels and an
  energy cross-check that repairs gaps. *(Always verify scanned values.)*
- **Neural offline voice** — an on-device announcer with selectable styles and
  effects. Fully offline.

## Requirements

- Android **8.0 (API 26)** or newer, **arm64-v8a** device.
- ~90 MB free space. Installs by sideloading the APK (not on the Play Store).

## Download & install

1. Open the [**Releases**](../../releases) page and download the latest
   `FindASet-<version>.apk`.
2. **Verify it** (strongly recommended — see below).
3. On your phone, open the APK and allow installing from this source if prompted
   ("Install unknown apps"). Follow the installer.

## Verify your download (authenticity)

Every release publishes the **SHA-256 checksum** of the official APK, in
[`SHA256SUMS.txt`](SHA256SUMS.txt) and in the release notes. Compute the checksum
of your downloaded file and confirm it matches **exactly**. If it does, you have
the genuine, unmodified build signed by the author. If it does **not**, do not
install it.

**v1.2 — `FindASet-1.2.apk`**

```
2539f5cf83b028619f6f6ab3f3d9ec19a47633893c606cefa9c4be7e9b78591e
```

Compute it yourself:

```bash
# Windows (PowerShell)
Get-FileHash .\FindASet-1.2.apk -Algorithm SHA256

# macOS
shasum -a 256 FindASet-1.2.apk

# Linux
sha256sum FindASet-1.2.apk
```

The APK is signed with the author's release key
(`CN=Marco Aurelio Fattizzo, O=FindASet, C=DE`); Android will refuse any later
update that is not signed with the same key.

## License

FindASet is **proprietary, closed-source** software — see [LICENSE](LICENSE).

In short: you may **use** it for any purpose, **private or commercial** (companies
may use it internally), **free of charge**. You may **not** redistribute, copy to
others, modify, create derivative works of, sell, rent, sublicense, or
reverse-engineer it. To share it, point people to this repository rather than
passing on the file. All rights reserved.

## Disclaimer

FindASet is a personal bookkeeping tool and is **not medical, dietary, or fitness
advice**, and **not** a medical device. Figures (including scanned label values)
are estimates — verify them yourself. Exercise carries risk; train within your
limits and consult a professional. You use the app at your own risk; provided
**"as is"** without warranty, with liability limited to the extent permitted by
law. Full terms in [DISCLAIMER.md](DISCLAIMER.md).

## Third-party components

The app bundles third-party open-source libraries (AndroidX / Jetpack Compose,
Kotlin, kotlinx.serialization, ML Kit, CameraX, sherpa-onnx) under their own
licenses — acknowledged in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

## Contact

Questions or reports: open an issue in this repository.
