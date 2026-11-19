# TS AI – Android starter project

This repository builds a TS AI Android APK using GitHub Actions.

## Build the APK
1. Upload the contents of this ZIP into the root of a new GitHub repository (not the ZIP file itself).
2. Open the repository's **Actions** tab.
3. Select **Build TS AI APK** and tap **Run workflow** (or wait for the automatic build after pushing to `main`).
4. Open the completed workflow run, scroll to **Artifacts**, and download `TS-AI-debug-apk`.
5. Extract the artifact ZIP and install `app-debug.apk` on your Android phone.

## Important: AI generation status
This project currently includes the TS AI Android shell, dark-purple UI, topic/script input switch, requested duration choices (30 seconds through 9 minutes), local saved-script library, and GitHub APK build workflow.

**Real AI generation is not connected in this ZIP.** The Generate button deliberately reports that a backend is not configured; it does not invent a fake result. A working AI service requires one of:
- a self-hosted model endpoint (hosting/GPU costs and capacity apply), or
- a provider account/key or user-authorized sign-in flow.

There is no reliable way to guarantee unlimited, fast, free hosted AI generation with zero setup. Do not paste a private API key into `index.html` or the APK. The secure next step is to connect a backend and store its credentials as server-side secrets.

## Project structure
- `app/src/main/java/.../MainActivity.java`: Android WebView shell
- `app/src/main/assets/index.html`: TS AI interface and local script library
- `.github/workflows/build-apk.yml`: GitHub Actions debug APK build

## Build requirements
GitHub-hosted Ubuntu runner, JDK 17, Gradle 8.9, Android Gradle Plugin 8.7.3.
