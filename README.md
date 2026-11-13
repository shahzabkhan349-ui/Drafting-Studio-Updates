# Drafting Studio Updates

This public repository hosts update metadata and Android release APKs for the Drafting Studio app.

## Update feed

The Android app checks:

`https://raw.githubusercontent.com/shahzabkhan349-ui/Drafting-Studio-Updates/main/latest.json`

Feed format:

```json
{
  "versionCode": 1,
  "versionName": "1.0",
  "releaseNotes": "Initial release",
  "apkUrl": "",
  "minimumSupportedVersionCode": 1
}
```

Future signed APKs will be attached to GitHub Releases and this feed will be updated to point to the latest release.

## Signing safety

Android permits an in-place update only when the package ID and signing certificate match. The first stable-signed build may require a one-time manual install if the currently installed APK was signed using a temporary CI debug key.

Never upload signing keystores or passwords to this public repository. Keep them only in GitHub Actions Secrets in the private source repository.
