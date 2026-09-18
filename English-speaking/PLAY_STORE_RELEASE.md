# English Speaking — Google Play release plan

## Current status
The project is a web/PWA prototype. It is not yet an Android APK or signed Android App Bundle. Do not upload the HTML file directly to Google Play.

## Required build steps
1. Wrap the web app with Capacitor or rebuild it in Flutter.
2. Add Android project files.
3. Configure package ID, for example `com.englishspeaking.app`.
4. Add app icon and adaptive icon.
5. Add splash screen.
6. Request microphone permission only when speaking starts.
7. Add a clear microphone permission explanation.
8. Build a signed Android App Bundle (`.aab`).
9. Test the release build on physical Android devices.
10. Upload to Play Console internal testing before production.

## Play Console requirements
- Developer account
- App name: English Speaking
- Short description
- Full description
- App icon
- Feature graphic
- Screenshots
- Privacy policy URL
- Data Safety form
- Content rating questionnaire
- Target audience declaration
- App access instructions, if login is added
- Signed Android App Bundle

## Privacy and data declarations
The current free mode should declare:
- Microphone access is used for speaking practice.
- Audio is not intentionally stored by the app.
- Progress is stored locally on the device.
- No account is required.
- Optional server AI features must be declared separately if enabled.

## Before production
- Replace the privacy policy contact placeholder.
- Test microphone denial and recovery.
- Test Android back button and rotation.
- Test offline launch.
- Test low-end devices.
- Confirm no API keys are inside the APK.
- Add crash reporting only after reviewing its privacy impact.
- Use internal, closed, and open testing tracks before production.
