# WaterFlow AI

A clean, lightweight, offline-first Android hydration tracker built with Kotlin + Jetpack Compose.

## Features (MVP)
- **Offline-first**: Uses Room Database for storing logs locally.
- **Smart Reminders**: Uses WorkManager to schedule gentle notifications only when you are behind schedule.
- **Quick Logging**: Log water intake with minimal taps.
- **Clean Architecture**: Repository pattern with ViewModel and Coroutines.

## Getting Started

1. **Clone the repository**.
2. **Open in Android Studio** (Ladybug or newer recommended).
3. **Sync Gradle**.
4. **Run** on an emulator or device (API 26+).

## Build Commands

```bash
# Assemble Debug APK
./gradlew assembleDebug

# Build Release Bundle (AAB)
./gradlew bundleRelease
```

## Signing (Release)

Generate a keystore:
```bash
keytool -genkey -v -keystore waterflow-release.jks -keyalg RSA -keysize 2048 -validity 10000 -alias waterflow
```

Configure `signingConfigs` in `app/build.gradle.kts` with your keystore details before release.

## License
MIT
