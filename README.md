# AppMaster

A small Windows tray app that bundles several everyday utilities, each one a module you can switch on or off. Free to use; the source code is not published.

| Module | What it does |
| --- | --- |
| Always on top | Pin any window above the others with a shortcut. |
| Auto click | Click again and again, at a picked spot or at the mouse cursor. |
| Clipboard | Keep everything you copy and paste any of it again later. |
| FancyZones | Snap windows into zones: drag a window while holding Shift and drop it on a zone. |
| Shutdown timer | Turn the PC off after a countdown. |
| Start menu | A classic Start menu in place of the Windows one. |
| Text extractor | Copy text from anywhere on the screen, even from pictures and videos. |
| Uninstaller | Remove programs and the files they leave behind. |
| Vietnamese typing | Type Vietnamese with Telex or VNI in any app. |
| Zip | Extract and create archives from Explorer's right-click menu. |

## Requirements

- Windows 10 version 1903 or newer, or Windows 11, 64-bit
- .NET Framework 4.8 (already part of those Windows versions, nothing to install)

## Install

1. Download `AppMaster-<version>.zip` from the [Releases](../../releases) page.
2. Extract it to a folder of your own, for example `C:\Tools\AppMaster`. Keep the `Data` folder next to the exe.
3. Run `AppMaster-<version>.exe`. The app lives in the tray; settings are saved in `settings.ini` next to the exe.

## Update

When a newer release exists, the Dashboard shows "Update available". Click it: AppMaster downloads the release zip, closes, replaces its own files and starts the new version. Your settings and clipboard history stay as they are.

To remove the app, turn off "Start with Windows" first (it removes the scheduled task the app created), then delete the folder.

## Good to know

- **Administrator rights.** The app asks for them (Auto click and Clipboard need to send input to elevated windows).
- **Unsigned exe.** Windows SmartScreen warns about it, and some antivirus tools may flag it, because the app uses global keyboard hooks and loads two small DLLs into Explorer (the Start menu taskbar hook and the Zip right-click menu). Every release lists the SHA-256 of the zip so you can check your download.
- **Clipboard history is stored on disk** in the `Clipboard` folder next to the exe (up to the history size you set). Data that password managers mark as secret is skipped. Delete the folder to clear it.
- **Network.** The app contacts `github.com` once a day to look for a newer release, and downloads that release only when you click the update.

## License

AppMaster is freeware; see [LICENSE](LICENSE). It includes `7z.dll` from 7-Zip under its own license; see [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).
