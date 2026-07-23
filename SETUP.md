# SplitLynx Setup Guide

Follow the section for your computer. No coding or command line is needed.

## Before you begin

Have these items ready:

1. Your SplitLynx license key.
2. Your brokerage username and password.
3. Your brokerage account number, if automatic discovery does not find it.
4. Your phone or authentication app for MFA.
5. A stable internet connection and the latest Google Chrome.

Install Chrome from <https://www.google.com/chrome/> and open it once before
starting SplitLynx. Chrome should be in its normal location—not inside Downloads
or running directly from an installer.

SplitLynx already includes its Python runtime, interface, scanner, broker
libraries, and other required program files. Do not install Python, Git,
Node.js, Homebrew, or any dependency package.

## Windows 10 or 11

### 1. Download the installer

Open the [latest release](https://github.com/drew109/SplitLynx-Releases/releases/latest)
and download `SplitLynx-<version>-Setup.exe`.

Only use a file downloaded from the `drew109/SplitLynx-Releases` repository.

### 2. Install SplitLynx

1. Double-click the Setup EXE.
2. If Windows asks whether the installer may make changes, choose **Yes**.
3. If Microsoft Defender shows an unknown-publisher warning, confirm that the
   filename and GitHub repository match, choose **More info**, then
   **Run anyway**.
4. Finish the installer for your current Windows account.
5. Open the new **SplitLynx** shortcut on the Desktop or Start menu.

Do not extract or move internal program files. The installer keeps them under
Local AppData and gives you one normal shortcut.

## macOS 13 Ventura or newer

### 1. Choose the correct Mac file

Choose **Apple menu > About This Mac**:

- `Apple M1`, `M2`, `M3`, `M4`, or `M5`: download the `macos-arm64` DMG.
- `Intel`: download the `macos-x64` DMG.

Using the wrong file will not damage the Mac, but the app will not run.

### 2. Install the app

1. Double-click the downloaded DMG.
2. Drag `SplitLynx.app` onto the **Applications** folder shown in the DMG.
3. Wait for copying to finish.
4. Eject the SplitLynx disk image.
5. Open Finder and select **Applications**.
6. Control-click `SplitLynx`, choose **Open**, then choose **Open** again.

The Mac packages are currently unsigned test builds. If macOS still blocks the
app:

1. Try to open SplitLynx once so macOS records the block.
2. Open **System Settings > Privacy & Security**.
3. Scroll to the security message about SplitLynx.
4. Choose **Open Anyway**, authenticate to the Mac if asked, then **Open**.

Do not disable Gatekeeper and do not paste commands into Terminal. When macOS
or Keychain asks for permission during account setup, read the prompt and allow
SplitLynx only if the app name and action are expected.

## First launch on Windows or Mac

### 1. Activate the app

1. Enter the license key supplied by the SplitLynx owner.
2. Choose **Activate**.
3. Keep the `TS-` key private. One key is linked to one computer.

If the key says it belongs to another device, contact the owner for a reset.
Reinstalling the app will not move a key to a different computer.

### 2. Add a brokerage account

1. Select **Tasks** in the left sidebar.
2. Choose **Add Task**.
3. Select the brokerage.
4. Enter the brokerage username and password.
5. Choose account discovery when offered. If discovery is unavailable or finds
   nothing, enter the brokerage account number manually and add it.
6. Save the task and make sure its **Enabled** switch is on.
7. Repeat these steps for each brokerage account you want SplitLynx to check.

Saved passwords are protected by the current Windows account on Windows and by
macOS Keychain on Mac. Never send a password or MFA code in a support log.

### 3. Log in to the brokerages

1. On **Tasks**, choose **Login All**.
2. Keep SplitLynx and any Chrome window open.
3. Complete MFA, login approval, or CAPTCHA when the brokerage asks.
4. Do not close the security window while SplitLynx is waiting.
5. Return to Tasks and confirm that the intended accounts remain enabled.

SoFi and some other brokerages may open a visible Chrome security flow. Finish
the CAPTCHA before changing login fields. If the brokerage rejects the login,
sign in to the brokerage normally, clear any security alert, and try
**Login All** again.

### 4. Start the scanner

1. Open **Status**.
2. Confirm that the server shows connected and that enabled accounts are listed.
3. Press **Start**.
4. Leave the app open while it scans. A valid candidate appears under
   **Pending Approval**; an empty list can simply mean there is no qualifying
   reverse-split trade at that moment.

SplitLynx monitors reverse-stock-split round-up opportunities only. It does not
automatically submit a candidate merely because the scanner finds one.

### 5. Review before accepting

Before choosing **Accept**, verify every item:

- the ticker symbol;
- Buy or Sell;
- quantity and displayed price;
- intended brokerage accounts; and
- the right stock is actually tradable on those brokerages.

Check only the trades you intend to submit, then choose **Accept**. Broker
restrictions, duplicate ownership, closed markets, MFA, and validation failures
can still prevent an order. Read the live log on the right for the exact result.

## Common fixes

### Chrome is not detected

1. Update Chrome from **Chrome menu > Help > About Google Chrome**.
2. Make sure Chrome is installed in `Program Files` on Windows or
   `/Applications` on Mac.
3. Open Chrome once, close it, restart SplitLynx, and try **Login All** again.

### A brokerage account is missing

Open **Tasks**, edit the task, add the exact brokerage account number manually,
save it, and confirm the task is enabled. Do not create a duplicate task for the
same brokerage login and account.

### Login, MFA, or CAPTCHA fails

Confirm the credentials by signing in directly at the brokerage, clear any
account-security warning, then retry. Slow Wi-Fi can make a login time out; wait
for a stable connection before retrying. Never approve an MFA request you did
not just start.

### Mac says the app cannot be opened

Confirm that you downloaded ARM64 for an Apple M-series Mac or x64 for Intel.
Move the app into Applications, eject the DMG, then use Control-click > Open.
If needed, use **Privacy & Security > Open Anyway** as described above.

### Start shows no pending trades

Check that the server is connected, the correct Tasks are enabled, and the
scanner has had time to refresh. The market can be closed and there may be no
qualifying filing. Do not create a manual trade only to test a live account.

### Something still does not work

1. Press **Log** in the sidebar.
2. Briefly describe what you clicked and what you expected.
3. Submit the report and save the displayed `TSLOG` reference.
4. Send only the reference to support.

The support report removes passwords, license keys, tokens, cookies, emails,
account numbers, balances, and complete holdings.
