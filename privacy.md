---
title: Privacy policy - Keep Your Credentials
---

# Privacy policy

Effective date: 30 October 2026

Keep Your Credentials ("the app") is a credentials manager that runs on your computer. This policy explains what data the app handles and where it goes.

## Summary

- The app has **no servers** and **no accounts** of its own. The developer receives no data from you.
- Your vault is **encrypted on your device** before it is saved or uploaded. Only someone with your master password can read it.
- If you connect Google Drive, the encrypted vault is stored in **your own** Google Drive, in a hidden folder that only this app can access.
- No analytics, no tracking, no advertising.

## Data stored on your device

- **Your vault** (the credentials you enter: names, URLs, usernames, passwords, descriptions, tags and folders) is stored in an encrypted file in the app's data folder. It is encrypted with XChaCha20-Poly1305 using a key derived from your master password with Argon2id.
- **The derived key** is cached in your operating system's keychain (Windows Credential Manager, or the Secret Service on Linux) so the app can unlock without asking every time. Locking the vault removes it. Your master password itself is never stored.
- **Sync bookkeeping** (which version of each item was last synced, unresolved sync conflicts, sync settings) is stored in a second encrypted file next to the vault.
- **Google sign-in token:** if you connect Google Drive, the refresh token Google issues is stored in your operating system's keychain.

## Google Drive

Connecting Google Drive is optional. When you connect it, you sign in to your own Google account in your browser and grant the app one permission:

- `https://www.googleapis.com/auth/drive.appdata`: see, create and delete the app's own configuration data in your Google Drive.

With this permission the app can only access its own hidden application folder (`appDataFolder`). It **cannot see, open or change any other file** in your Drive.

The app uses this folder to store one file: your vault, **encrypted on your device before upload**. Google stores this encrypted file but cannot read its contents, and neither can the developer. The app downloads it to merge changes made on your other devices.

The app's use of information received from Google APIs adheres to the [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy), including the Limited Use requirements. Data from Google Drive is used only to sync your own vault between your own devices. It is not transferred to anyone, not used for advertising, and not read by humans.

## Network connections

The app connects only to:

- **Google** (accounts.google.com, oauth2.googleapis.com, www.googleapis.com), and only if you connect Google Drive: to sign in and to upload and download your encrypted vault.
- **GitHub** (github.com, objects.githubusercontent.com): to check for and download app updates. These requests contain no personal data.
- Websites you open yourself with the app's "Open" button, in your browser.

## Removing your data

- **From Google Drive:** choose *Disconnect* in the app's sync settings, and remove the app's access at <https://myaccount.google.com/permissions>. To delete the stored file, use *Manage apps* in Google Drive's settings and delete Keep Your Credentials' hidden data.
- **From your device:** uninstall the app and delete its data folder (`%APPDATA%\com.keepyourcredentials.app` on Windows, `~/.local/share/com.keepyourcredentials.app` on Linux).

## Children

The app is not directed at children under 13 and collects no personal information from anyone.

## Changes

If this policy changes, the new version will be published on this page with a new effective date.

## Contact

Questions about this policy: koussawojeandev@gmail.com
