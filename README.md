# VoxWolf Dictation

VoxWolf is a native Android prototype that lets you dictate directly into whatever text field is currently focused, using an accessibility service and fully on-device speech recognition.

## Features

- Continuous microphone capture streamed to an on-device [whisper.cpp](https://github.com/ggml-org/whisper.cpp) engine for transcription — no network connection required, works even in airplane mode
- Accessibility service with a floating control for starting and stopping dictation
- Foreground listening notification while dictation is active
- Cursor/selection-aware text insertion into the focused editable field
- Password-field blocking, so dictation never activates on secure inputs
- Local cleanup pass for spoken punctuation before text is inserted

## Getting started

1. Install Android Studio with Android SDK 35 and JDK 17.
2. Open this project in Android Studio and let it sync Gradle.
3. Connect an Android 12+ device with USB debugging enabled.
4. Select the device and run the app.

## Using VoxWolf on your phone

1. Open the app and grant the microphone permission.
2. Tap **Enable typing service**.
3. Enable **VoxWolf typing service** under Android's Accessibility settings.
4. In any app, place the cursor in a text field and tap the floating **W** icon to start dictating.
5. Tap **STOP** to end dictation.

## Continuous integration

This repository runs a basic GitHub Actions workflow on pushes and pull requests to `main` (see `.github/workflows/blank.yml`).
