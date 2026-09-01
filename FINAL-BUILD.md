# M1 HARIOM 1.0.0 — Phone-only APK build

## GitHub Actions
1. Put this project in the `M1-hariom` repository on GitHub.
2. Open **Actions**.
3. Select **Build M1 HARIOM APK**.
4. Choose **Run workflow** (or push to `main`).
5. Wait for the green check.
6. Open the completed run and download the **M1-Hariom-APK** artifact.
7. Extract the downloaded artifact on your phone if necessary and install the APK.

The workflow runs unit tests before building the APK. It uses a GitHub-hosted Ubuntu runner, JDK 17, Android SDK 35, and Gradle 8.10.2.

## Important Android behavior
- Android may ask you to allow installation from the app you used to open the APK.
- Exact-alarm permission, notification permission, camera permission, and activity-recognition permission are requested/handled only when relevant.
- Battery optimization varies by manufacturer. Use the in-app reliability guidance if an OEM restricts background alarms.

## Release
The included workflow intentionally produces a debug APK for simple sideloading. A Play Store release should use a securely managed signing key and an AAB/release workflow; never commit signing keys or passwords to this repository.
