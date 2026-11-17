# Android Adware Check

An open agent skill for diagnosing intrusive Android ads on a USB-connected device with ADB, without root. It helps an assistant trace full-screen ad activities and notifications, review relevant permissions, and explain evidence before targeted remediation.

This is not an antivirus or a guarantee that a device is clean. It cannot reliably identify every malicious app or prevent all future ads. The device owner remains in control of changes; uninstalling can remove app data.

## Use

Install or copy `skills/android-adware-check` into your agent's skills directory, then ask your agent to use `android-adware-check` on an authorized Android device connected by USB. Android Platform Tools (`adb`) and USB debugging authorization are required. Android versions and device manufacturers expose different diagnostics.

## Privacy

The skill does not require uploading device data. Diagnostic outputs can contain private information; review anything before sharing it.
