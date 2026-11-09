# Blood Pressure Log

A single-page blood pressure tracker: log systolic / diastolic / pulse with scroll wheels, browse history, see statistics and trends.

## Features
- **Add** – wheel pickers, date, time, tags and notes; live classification gauge
- **History** – grouped by day, tap a reading to edit or delete
- **Stats** – averages, min/max, trend chart, classification breakdown, morning vs evening (7D / 30D / 90D / 1Y / All)
- **Themes** – Light, Dark, Black (AMOLED), System
- **Import / export** – CSV (auto-detects columns and date format, skips duplicates)

## Classification
| Type | SYS | DIA |
|---|---|---|
| Stage 2 Hypertension | > 160 | > 100 |
| Stage 1 Hypertension | 141–160 | 91–100 |
| Prehypertension | 121–140 | 81–90 |
| Normal | 91–120 | 61–80 |
| Hypotension | < 90 | < 60 |

## Storage
Hosted as a Claude artifact, readings sync privately to the owner's Claude account.
Opened anywhere else (e.g. GitHub Pages or a local file), it falls back to the browser's localStorage.

Personal data exports (`*.csv`) are git-ignored and should not be committed.

## Android APK
Every push to `main` builds an APK with GitHub Actions (Capacitor WebView wrapper) and publishes it under **Releases**.
In the APK, readings are stored on the phone (localStorage); use Settings → Import / Export to move data.
The signing key in `android-keystore/` is a personal sideload key, so updates install over each other without losing data.
