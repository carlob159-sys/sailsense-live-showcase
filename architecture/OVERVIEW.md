# SailSense Live — architecture overview (public)

Mobile sailing instrument app (Android primary, iOS port in progress).

## Layers

- **Sensors:** GPS (high-rate), accelerometer, magnetometer/compass
- **Signal processing:** heel, trim, SOG/COG, TWA, VMG, dead reckoning when needed
- **Coach UI:** high-contrast targets (green/red), boat mode (touch lock, REC, calibrate, match)
- **Recording:** background logging + CSV export for post-race analysis (Sailing Analyzer compatible)
- **Privacy:** offline-first; no cloud required for core coaching

## Commercial model

Paid mobile product (Play Store / direct). This repository is a **product & architecture showcase** only.
Full application source, signing keys, and store builds are **private**.

## Related public work

- https://github.com/carlob159-sys/Sailing-Analizer
- https://github.com/carlob159-sys/waszp-sail-number-cv
