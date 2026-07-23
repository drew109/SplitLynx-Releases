# SplitLynx Downloads

This is the official public download page for SplitLynx. It contains compiled
installers only; the source code and release tools remain private.

## Download

Open the [latest release](https://github.com/drew109/SplitLynx-Releases/releases/latest)
and choose exactly one file:

| Computer | File to download |
| --- | --- |
| Windows 10 or 11, 64-bit | `SplitLynx-<version>-Setup.exe` |
| Mac with an Apple M1, M2, M3, M4, or M5 chip | `macos-arm64` DMG |
| Older Mac with an Intel processor | `macos-x64` DMG |

On a Mac, choose **Apple menu > About This Mac**. If **Chip** starts with
`Apple M`, use ARM64. If **Processor** says `Intel`, use x64.

## What must already be ready

- A SplitLynx license key from the owner.
- A reliable internet connection.
- The latest [Google Chrome](https://www.google.com/chrome/) installed normally.
- Brokerage login details, account number, and access to any MFA or CAPTCHA.

Python, Git, Node.js, command-line tools, and separate dependency folders are
**not required**. Everything except Chrome is bundled in the installer/app.

## Install and start

- **Windows:** download the Setup EXE, double-click it, finish the installer,
  then open the new SplitLynx Desktop or Start-menu shortcut.
- **Mac:** download the correct DMG, open it, drag `SplitLynx.app` into
  **Applications**, eject the DMG, then Control-click SplitLynx in Applications
  and choose **Open** for the first launch.

Continue with the complete non-technical instructions in
**[SETUP.md](SETUP.md)**. They cover activation, Chrome, adding brokerage
accounts, MFA/CAPTCHA, starting the scanner, approving a trade, and fixing
common setup problems.

## Automatic updates

SplitLynx 1.3.37 and newer checks for updates when it opens. On Windows, choose
**Install Update** to download and verify the package while a progress bar is
shown. SplitLynx closes only after the package is ready, installs it, reopens
automatically, and shows a green **Successfully updated** message.

Version 1.3.36 had a broken installer handoff. If 1.3.36 says an update was
scheduled but does not close, download the latest Windows Setup EXE from this
repository and run it once. Automatic updates work normally after 1.3.37 is
installed.

## Important Mac note

The current Mac packages are unsigned test builds. macOS may require
**System Settings > Privacy & Security > Open Anyway** after the first launch
attempt. Do not disable Gatekeeper and do not run Terminal commands.

Use a test or low-risk account first. Always read the symbol, brokerage,
quantity, and price in **Pending Approval** before pressing **Accept**.

## Support

Press **Log** in the SplitLynx sidebar and briefly describe what happened. The
report is sanitized before upload and provides a `TSLOG` reference for support.
Saved passwords, license keys, tokens, emails, account numbers, and balances are
excluded.
