# Jigglo - Windows Tray Mouse Jiggler

Jigglo is a small Windows tray utility that gently moves the mouse at intervals to keep your PC from going idle while you are watching, reading, or running long jobs.  
It is **free for personal use** (see `LICENSE.txt` for full terms).

---

## What This Repository Contains

- The **personal-use license**: `LICENSE.txt`
- A **user manual**: `MANUAL.txt`
- A convenience build archive: `Jigglo-0.1.1-win-x64.zip` (same contents as the public release ZIP)
- A work-in-progress Windows project under `Jigglo/Jigglo/` used for development.

Official end-user downloads are published on GitHub Releases in the separate `azenkwed/jigglo-releases` repository by the same author.  
The code in `Jigglo/Jigglo/` does **not** currently represent the full production source for the released binary.

---

## Download (Official Builds)

- Latest version: **0.1.1**
- GitHub Releases (recommended):  
  [`Jigglo-0.1.1-win-x64.zip`](https://github.com/azenkwed/jigglo-releases/releases/tag/v0.1.1)

After downloading from GitHub Releases:

1. Right-click the ZIP and choose **Extract All…**.
2. Extract to a folder you trust (for example, `C:\Users\<you>\Apps\Jigglo`).
3. Run `Jigglo.exe`.

System requirements:

- Windows 10 or later (64-bit).
- .NET Framework 4.8 (included with most Windows 10/11 installs; keep Windows Update current).

---

## Features (What Jigglo Does)

- Runs quietly as a **system tray icon**.
- Tray menu with:
  - **Start jiggling / Stop jiggling** toggle.
  - Interval options: 15s, 30s, 1m, 2m, 4m.
  - Jiggle size options: small, medium, large.
  - **Auto-start when idle** toggle (4 minutes idle threshold).
  - **Launch at login** toggle using the current user's `Run` registry key.
- Per-user settings stored under `%APPDATA%\Jigglo\settings.json`.

When **Auto-start when idle** is enabled, Jigglo will automatically resume jiggling after you've been idle for about 4 minutes, even if you previously stopped it manually.

For more detailed usage instructions, see `MANUAL.txt`.

---

## Trust, Security & Antivirus

Jigglo is intentionally simple and local-only:

- **No network access**: it does not talk to the internet, check for updates, or send telemetry.
- **What it touches**:
  - Simulates small mouse movements via standard Windows APIs.
  - Optionally writes a single value under  
    `HKCU\Software\Microsoft\Windows\CurrentVersion\Run` to enable “Launch at login”.
  - Stores a small JSON settings file under `%APPDATA%\Jigglo\settings.json`.

Because Jigglo moves the cursor and can start with Windows, some antivirus tools or Windows SmartScreen may warn on first run. That is expected behavior for small utilities like this.

If your security tools flag Jigglo:

- Prefer adding `Jigglo.exe` as an allowed/trusted app **only if you are confident in the binary and trust the source**.
- **Do not** disable your antivirus or other protections globally.

Jigglo is not currently code-signed, so SmartScreen may show _“Windows protected your PC”_ on first run. If (and only if) you downloaded from the official GitHub release and trust it, you can use **More info → Run anyway**.

To verify the integrity of the 0.1.1 ZIP:

- `Jigglo-0.1.1-win-x64.zip` SHA-256:  
  `293E8234FBE84327EF01059ED6086CD48EE898A01281E319BCED61DDCE3C069E`

You can compute the SHA-256 hash on your machine and confirm it matches this value before extracting.

---

## Workplace / IT Policies (Please Read)

Jigglo can interfere with power-saving and lock-screen policies by design. On **work, school, or otherwise managed devices**:

- Always treat Jigglo like any other third‑party utility.
- If your organization has policies about screen locking, idle timeouts, or installing software, **you must follow those policies**.
- Do **not** use Jigglo (or any similar tool) to deliberately bypass security or compliance requirements set by your IT department or employer.
- When in doubt, ask your IT team before installing or running Jigglo on a managed device.

Using tools like this against your organization's policies can be a serious issue; you are responsible for how and where you use Jigglo.

---

## License

Jigglo is distributed under a **Free for Personal Use** license (`LICENSE.txt`):

- You may use Jigglo for your own personal, non-commercial use.
- Commercial use, redistribution, and modification are restricted; see the license text for details.

The current public repository does **not** contain the complete production source code for the released binary. If/when the full source is published, this README will be updated to point to it.

---

## How Jigglo Compares to Alternatives

Other tools already exist that can keep Windows awake, including:

- **PowerToys Awake** (from Microsoft’s PowerToys suite)
- **The Wiggler** (Microsoft Store app)

Jigglo's focus is:

- A **single-purpose, minimal tray app** dedicated to gentle mouse jiggling.
- **Transparent behavior**: no network, no auto-update, simple settings stored under your user profile.


If you prefer a Microsoft-backed solution or a Store-distributed app, PowerToys Awake or The Wiggler may be better fits for you. Jigglo exists for people who specifically want a small, self-contained mouse jiggler they can inspect and run on their own devices.

---

## Support Jigglo

If Jigglo helps you and you’d like to support development:

- Ko-fi: https://ko-fi.com/azenkwed

The tray menu includes a **Support Jigglo** item that opens this link.

Advanced users can override the support link by setting a `JIGGLO_SUPPORT_URL` environment variable to any URL (for example, your own mirror or donation page).
