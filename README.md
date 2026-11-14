# Personal Money Tracker (starter)

A small native Android starter project for a personal KPay/Wave notification tracker.
It uses Kotlin + Android SDK + SQLite. There is no Node.js backend and no cloud backend.

## Important limitations
- The app reads only notifications from package names explicitly added to its allowlist.
- Notification access must be enabled manually in Android Settings.
- It cannot query the actual wallet balance or transaction ledger.
- Notification text formats vary. The included amount and direction parser is only a starter and must be tested against real, redacted notification examples.
- Do not use this as the sole proof of payment. Verify important payments in the official wallet app.
- Data is stored locally on the phone. No notification content is sent to a server.

## Build without installing Android Studio locally
1. Create a GitHub repository and upload this project.
2. Push to the `main` branch (or use Actions > Build Android APK > Run workflow).
3. Open the workflow run and download the `money-tracker-debug-apk` artifact.
4. Extract it and install `app-debug.apk` on your Android phone.

## Work in VS Code
Open this folder in VS Code. Edit Kotlin files under:
`app/src/main/java/com/kairoo/moneytracker/`

## First-run setup
1. Install the APK.
2. Open the app and tap **Open notification access settings**.
3. Enable access for Money Tracker.
4. Add only the KPay and Wave app package names to the allowlist, one per line.
5. Save allowed apps.
6. Make a small test transaction and compare the captured notification with the official wallet app.

## Next development step
The exact KPay and Wave package names and redacted notification examples are needed to tune the allowlist and parser. Never share OTPs, phone numbers, account identifiers, or full transaction references.
