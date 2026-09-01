# M1 HARIOM — Do the M1 Boy

## Build 0.3

This checkpoint adds the first real M1 challenge workflow on top of the alarm foundation.

### Challenge features
- QR challenge registration by scanning a physical QR code with the camera.
- Barcode challenge registration by scanning a supported physical barcode.
- QR/barcode verification on the ringing screen.
- Wrong codes do not dismiss the alarm.
- QR mode accepts QR Code format; barcode mode rejects QR Code format.
- Camera scanning does not offer gallery import.
- Challenge secrets remain in the local alarm data store; no account or cloud service is required.
- Challenge types are represented through a registry/contract so additional challenges can be added without rewriting alarm scheduling.

### Phone-only APK build
The repository includes `.github/workflows/build-apk.yml`.

On GitHub: **Actions → Build M1 HARIOM APK → Run workflow**. The workflow builds the debug APK on a GitHub-hosted runner and uploads it as the `M1-Hariom-APK` artifact.

No Android Studio is required for this cloud build workflow.

### Current scope
This is a development checkpoint, not the final release. Advanced challenge types, complete analytics, streaks, backup/restore, reliability hardening, and release signing remain planned for later checkpoints.

## Build 0.4 — Advanced Challenges
- Added reusable challenge factory for difficulty-scaled math and memory challenges.
- Added memory-sequence dismissal flow.
- Added motion-based shake challenge using the accelerometer.
- Added step challenge using Android's step detector when available.
- Added multi-step challenge framework and sequential math/code progression.
- Added challenge difficulty, step target, and multi-step fields to persisted alarm data.
- Added activity-recognition permission for step detection.

### Device limitations
Sensor availability varies by phone. If a required sensor is unavailable, the app reports this instead of silently dismissing the alarm. NFC and location remain reserved for a later device-specific implementation.

## Build 1.0 — Data, export, and release readiness
- Versioned local JSON backup/restore for alarms and analytics.
- CSV analytics export.
- PDF insights report generated on-device.
- Import validation with backup format/version checks.
- No cloud account is required for backup/export.
- GitHub Actions remains the phone-friendly build path.
