# သားကြီး AI — Android starter project

This is an Android Studio Java project for an Android voice/chat assistant UI.

## Current features
- Burmese-labelled chat interface with blue theme
- Android speech recognition button (device/provider must support Burmese `my-MM`)
- Android TextToSpeech output (Burmese voice availability depends on the device)
- HTTPS backend integration point

## Important: AI connection is not configured yet
The app intentionally does not contain an AI provider API key. Do not put a private API key in an APK.

1. Deploy a small HTTPS backend that accepts `POST /chat` with JSON `{ "message": "..." }`.
2. Return JSON `{ "reply": "..." }`.
3. In `app/src/main/java/com/thargyi/ai/MainActivity.java`, replace `https://YOUR_BACKEND_DOMAIN/chat` with your backend URL.
4. Have the backend call your chosen AI provider using a secret stored on the server.

## Build APK
1. Open this folder in Android Studio (recent stable version).
2. Allow Gradle sync and install Android SDK Platform 35 if prompted.
3. Select **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
4. Android Studio will show the generated APK location, normally `app/build/outputs/apk/debug/app-debug.apk`.

The project source is provided here; a compiled APK has not been produced in this environment because Android SDK/Gradle build tools are not installed.
