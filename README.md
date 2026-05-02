# Asset Flow Desktop Beta Install Guide

Public beta installers and update metadata for Asset Flow Desktop are published in this repository. Use the latest GitHub Release for downloads.

Asset Flow Desktop is currently distributed as a controlled beta. The app is safe to use if you received the download link from the Asset Flow team, but the installers are not yet signed with paid Apple or Windows publisher certificates. Your computer may show security warnings on first install.

Download Asset Flow only from the official release link sent by the Asset Flow team.

## macOS

### Choose The Correct Download

- Apple Silicon Macs, including M1, M2, M3, and newer: download the `arm64` DMG.
- Intel Macs: download the `x64` DMG.

If macOS says the app is not supported on this Mac, delete it and install the other DMG.

### Install

1. Open the downloaded `.dmg`.
2. Drag `Asset Flow` into `Applications`.
3. Open `Applications`.
4. Double-click `Asset Flow`.
5. If macOS warns that Apple cannot verify the app, click `Done` or close the warning.
6. Follow the Privacy & Security steps below.
7. Log in with the account provided by the Asset Flow team after the app opens.

### Allow The App In Privacy & Security

1. Open `System Settings`.
2. Go to `Privacy & Security`.
3. Look for a message saying `Asset Flow` was blocked.
4. Click `Open Anyway`. It may ask you twice and may ask for your password.
5. Try opening `Asset Flow` again from `Applications`.

### Alternate macOS Open Method

If the Privacy & Security message does not appear, try this:

1. Open `Applications`.
2. Right-click `Asset Flow`.
3. Click `Open`.
4. If macOS warns that Apple cannot verify the app, click `Open` again if the option is shown.

### If There Is No Open Anyway Button

Only use this command for the Asset Flow beta app downloaded from the official release link.

1. Open `Terminal`.
2. Run:

   ```sh
   xattr -dr com.apple.quarantine /Applications/Asset\ Flow.app
   ```

3. Open `Asset Flow` again from `Applications`.

If macOS still blocks it, run:

```sh
codesign --force --deep --sign - /Applications/Asset\ Flow.app
xattr -dr com.apple.quarantine /Applications/Asset\ Flow.app
```

Then open `Asset Flow` again.

## Windows

### Install

1. Download the Windows `.exe` installer from the official release link.
2. Run the installer.
3. If Windows Defender SmartScreen appears, click `More info`.
4. Click `Run anyway`.
5. Complete the installer.
6. Open `Asset Flow` from the Start menu.
7. Log in with the account provided by the Asset Flow team.

### If Windows Warns About Unknown Publisher

This is expected during the beta because the Windows installer is not yet code-signed with a paid publisher certificate. Continue only if the installer came from the official Asset Flow release link.

## Permissions The App Needs

- Network access for login, project data, uploads, and downloads.
- File picker access when selecting files to upload.
- Folder picker access when choosing where downloads should be saved.

## Reinstalling

If support asks you to reinstall from scratch, remove the installed app first, restart your computer, then install the latest beta from the newest GitHub Release.
