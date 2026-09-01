# M1 HARIOM — Build 0.6

## What's new
- Versioned JSON backup and restore for alarms and analytics.
- CSV export of analytics history.
- On-device PDF insights report.
- Import validation and safe failure handling.
- Local-first data transfer; no account/cloud required.
- GitHub Actions cloud APK build no longer requires a checked-in Gradle wrapper: the workflow provisions Gradle 8.10.2 directly.

## Phone-only APK
GitHub → Actions → Build M1 HARIOM APK → Run workflow → open the successful run → Artifacts → M1-Hariom-APK.

The debug APK is intended for personal/local sharing. A future Play Store release should use a separately managed signing key and release AAB.
