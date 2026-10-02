# MY ID — Android App

This repository is prepared to build a downloadable Android APK with **GitHub Actions**.

## Easiest way to get the APK

1. Upload/push this project to a GitHub repository.
2. Open the repository on GitHub.
3. Go to **Actions**.
4. Select **Build Android APK** / **Build Android APK** workflow.
5. Tap **Run workflow** if it has not started automatically.
6. Wait until the green check appears.
7. Open the completed workflow run.
8. Scroll to **Artifacts**.
9. Download **MY_ID-APK**.
10. Extract the ZIP and install **MY_ID.apk** on your Android phone.

Every push to `main` or `master` also starts an automatic APK build.

## Project

- App name: MY ID
- Application ID: `com.aistudio.myid.vortex`
- Minimum Android version: API 24
- Target Android version: API 36
- Build type used by GitHub Actions: Debug APK

## Local build

If Android Studio is installed:

```bash
gradle :app:assembleDebug
```

The APK will be created at:

```text
app/build/outputs/apk/debug/app-debug.apk
```

## Important

The GitHub workflow intentionally builds the **Debug APK** so no private release keystore or passwords are required. This makes the repository safe to upload without putting signing credentials in GitHub.

For a Play Store release, create a separate release/upload-key setup and keep the keystore/passwords in GitHub Secrets. Do not upload private keystore files or passwords to the repository.
