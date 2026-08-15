# Kitti — Native Android Voice Assistant

Kitti is a Kotlin + Jetpack Compose Android assistant starter designed for low/mid-range phones. It uses Android's official speech recognition, Text-to-Speech, intents, alarms, settings screens, contacts/calling permission flow, and the Android VoiceInteractionService hook.

## Important: no fake unlimited access
Android does not allow an ordinary app to have unrestricted access to WhatsApp private data, Gmail account data, SMS contents, screen recording, or every system control. Kitti therefore never bypasses Android security. Sensitive operations remain user-controlled.

## No API key required
This build has **no AI/API configuration key**. The included intent engine is local and deterministic, so an APK build does not ask for an API key. An optional cloud LLM can be added later without putting a secret key in the APK.

## Build
Open this folder in Android Studio and let Gradle sync. Then choose **Build > Build APK(s)**. The generated debug APK will be under `app/build/outputs/apk/debug/`.

Recommended: Android Studio with JDK 17, Android SDK 35.

## Low-device design
- minSdk 26
- Compose UI kept small
- No bundled ML model
- No continuous audio recording by default
- No cloud service required for basic commands

## Voice assistant mode
To use Kitti from outside the app, Android may require the user to select Kitti as the device's default digital assistant/voice assistant. This is controlled by Android; Kitti cannot silently make itself the default assistant.

## Current supported examples
- Open YouTube, WhatsApp, Instagram, Facebook
- Camera, Settings, Wi-Fi, Bluetooth
- Google web search
- 10-minute timer and alarm screen
- Contact lookup + Android call flow
- WhatsApp message draft flow (review/send remains user-controlled)
- Gmail compose screen
- Bengali/English/Arabic/Hindi response language detection

## SMS / unknown caller alerts
The manifest contains SMS permission hooks for future compliant work, but the receiver intentionally does not read SMS content. SMS permissions are heavily restricted on Google Play and Android. A production version should use the appropriate default-SMS or supported role/workflow if distribution policy allows it.

## Security
Kitti does not attempt root access, accessibility abuse, permission bypass, credential extraction, private-app database access, or silent screen recording. Keep Android, Google Play Protect, and Kitti updated.
