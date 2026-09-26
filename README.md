# ShiftFlow releases

Public distribution channel for ShiftFlow Android updates. This repository contains
only public release documentation, `latest.json`, and signed APKs attached to GitHub Releases.
Application source code is maintained separately.

No signed release has been published yet. The initial manifest has `versionCode: 0`
and null download, checksum and publication fields, so installed apps will not offer an update.

## Updates

ShiftFlow checks `https://raw.githubusercontent.com/suzukits1995/ShiftFlow-Releases/main/latest.json`.
When a newer version is published, the app offers to download it, verifies its SHA-256
and package identity, and opens Android's package installer for your confirmation.
Android may first ask you to allow installations from ShiftFlow.

`latest.json` fields:

- `versionCode`: increasing Android version code (integer).
- `versionName`: display version.
- `apkUrl`: public HTTPS URL of the signed APK in this repository's Releases.
- `sha256`: lowercase SHA-256 of that APK.
- `releaseNotes`: plain-text release notes.
- `publishedAt`: UTC ISO 8601 publication timestamp.

Use the same signing identity for successive releases. Debug APKs use a different
identity and cannot be upgraded in place to a production-signed APK. Export a backup
before manually switching installations; uninstalling removes app data.

Never add source code, credentials, signing keys, backups or personal data here.
