# Jigglo Releases

This repository hosts public Windows builds of **Jigglo**, a lightweight tray utility that gently moves the mouse to keep your PC from going idle.

## Download

- Latest version: **0.1.1**
- Download ZIP: [`Jigglo-0.1.1-win-x64.zip`](https://github.com/azenkwed/jigglo-releases/releases/tag/v0.1.1)

Extract the ZIP somewhere you trust (for example, `C:\Users\<you>\Apps\Jigglo`) and run `Jigglo.exe`.

## Requirements

- Windows 10 or later (64-bit).
- .NET Framework 4.8 (included in Windows 10 and 11 on most systems; make sure your system is up to date).

## Features

- Tray icon with:
  - **Start jiggling / Stop jiggling** toggle.
  - Interval submenu: 15s, 30s, 1m, 2m, 4m.
  - Jiggle size submenu: small, medium, large.
  - **Auto-start when idle** toggle (4 minutes idle threshold).
  - **Launch at login** toggle using the current user's `Run` registry key.
- Settings stored under `%APPDATA%\Jigglo\settings.json`.

When **Auto-start when idle** is enabled, Jigglo will automatically start jiggling again after you've been idle for 4 minutes, even if you previously stopped it.

## Security & Antivirus

Jigglo simulates small mouse movements and writes a value under `HKCU\Software\Microsoft\Windows\CurrentVersion\Run`. Some antivirus tools may prompt when you first run it or enable launch-at-login.

If you trust this binary and your AV flags it:

- Prefer adding `Jigglo.exe` as a trusted/excluded application.
- Avoid disabling your antivirus globally.

Because Jigglo is currently not code-signed, Windows SmartScreen may show a "Windows protected your PC" warning the first time you run it. If you downloaded Jigglo from the official repository and trust it, you can choose **More info -> Run anyway**.

To verify the 0.1.1 ZIP you downloaded, you can compare its SHA-256 hash:

- `Jigglo-0.1.1-win-x64.zip` SHA-256: `293E8234FBE84327EF01059ED6086CD48EE898A01281E319BCED61DDCE3C069E`

## Support Jigglo

If Jigglo helps you, you can support development here:

- Ko-fi: https://ko-fi.com/azenkwed

You can also open this link from the tray menu via **Support Jigglo**.

Advanced users can override the support link by setting a `JIGGLO_SUPPORT_URL` environment variable to any URL (for example, your own mirror or donation page).
