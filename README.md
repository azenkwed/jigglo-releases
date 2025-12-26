# Jigglo Releases

  This repository hosts public Windows builds of **Jigglo**, a lightweight tray utility that
  gently moves the mouse to keep your PC from going idle.

  ## Download

  - Latest version: **0.1.0**
  - Download ZIP: [`Jigglo-0.1.0.zip`](./Jigglo-0.1.0.zip)

  Extract the ZIP somewhere you trust (for example, `C:\Users\<you>\Apps\Jigglo`) and run
  `Jigglo.exe`.

  ## Requirements

  - Windows 10 or later (64-bit)
  - .NET 8 Desktop Runtime

  ## Features

  - Tray icon with:
    - **Start jiggling / Stop jiggling** toggle
    - Interval submenu: 15s, 30s, 1m, 2m, 4m
    - Jiggle size submenu: small, medium, large
    - **Auto-start when idle** (4-minute idle threshold)
    - **Launch at login** using the current user's `Run` registry key
  - Settings stored under `%APPDATA%\Jigglo\settings.json`

  ## Security & Antivirus

  Jigglo simulates small mouse movements and writes a value under
  `HKCU\Software\Microsoft\Windows\CurrentVersion\Run`. Some antivirus tools may prompt when
  you first run it or enable launch-at-login.

  If you trust this binary and your AV flags it:

  - Add `Jigglo.exe` as a trusted / excluded application
  - Avoid disabling your antivirus globally