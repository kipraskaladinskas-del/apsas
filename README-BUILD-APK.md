# Build Noir APK on GitHub Actions (Windows-friendly)

This project can be built in GitHub's cloud runner, so you do not need to install Android Studio or the Android SDK on your Windows PC.

## Steps

1. Sign in to https://github.com/ and create a **private** repository named `noir-app`.
2. Upload the contents of this folder to the repository root. The root must contain `settings.gradle`, `build.gradle`, and the `app` folder. Make sure `.github/workflows/build-apk.yml` is included.
3. Commit the files to the `main` branch. GitHub Actions should start the **Build Noir APK** workflow automatically.
4. In the repository, open **Actions** → **Build Noir APK** → the latest completed run.
5. Under **Artifacts**, download `Noir-debug-apk`. Extract the downloaded artifact ZIP to get `app-debug.apk`.
6. Upload `app-debug.apk` to the Android APK hosting service you choose, if you want a share link or QR code.

## Notes

- This workflow creates a **debug APK** for testing/sharing, not a production-signed release APK.
- Anyone installing a shared APK may need to allow installation from that browser/source on Android.
- Do not commit API keys, passwords, signing keys, or private user data.
- This APK is for Android only. It cannot be installed on an iPhone and is not an iOS/TestFlight build.
