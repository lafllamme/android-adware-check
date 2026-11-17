# Android Adware Check

![Android via ADB](https://img.shields.io/badge/Android-ADB-3DDC84?style=flat) ![No root required](https://img.shields.io/badge/Root-not%20required-68866c?style=flat)

<img src="https://i.imgur.com/uiCNl9u.png" alt="Android Adware Check cover" width="100%">

Find out which Android app is behind unwanted ads. This AI agent skill helps you investigate and clean up over USB — no root required.

## Why this exists

My mother came to me convinced her Android phone had a virus and was broken. Every few seconds, a full-screen ad took over the display. Closing one just made room for the next. The phone had become almost impossible to use.

At first, I couldn't tell whether Chrome notifications or an installed app were responsible. An AI assistant used ADB to inspect the phone over USB and identify the apps behind the ad screens. There was more than one. Removing them stopped the interruptions. This skill grew out of that experience.

## What it checks

- The ADB connection and USB debugging authorization.
- The foreground app, recent activities, and active notifications.
- Installed apps and relevant special permissions, where available.
- Whether ads return after a targeted change.

The agent explains what it observed and what remains uncertain. App names, permissions, and store origin alone are not proof of malware. It prefers reversible changes and asks before uninstalling a named app, which may delete its local data.

## Requirements

- An Android device you are authorized to inspect, connected by USB.
- USB debugging enabled and the computer authorized on the device (the agent can guide you).
- [Android SDK Platform Tools](https://developer.android.com/tools/releases/platform-tools), including `adb` (the agent can help install them).
- A skill-compatible agent with terminal access to the connected computer.

## Install

Paste this into Claude, Codex, or another skill-compatible agent:

```text
Install the skill from https://github.com/lafllamme/android-adware-check (skills/android-adware-check).
```

Or install it from your terminal with the [Skills CLI](https://skills.sh/):

```bash
npx skills add lafllamme/android-adware-check
```

Choose your agent and installation scope when prompted. Node.js and `npx` are required.

## Use

Connect the Android device by USB and ask your agent:

> Use Android Adware Check to investigate unwanted ads on this phone.

The agent checks for ADB and offers to help install it if needed. It can guide you through connecting the phone and enabling USB debugging. If an ad appears, leave it visible while the agent checks which app is showing it.

## Use without installing

Prefer a quick prompt? Give this to an agent with terminal access to the computer connected to your phone:

```text
Help me investigate unwanted ads on my Android phone over USB using ADB, without root. If ADB or USB debugging isn't ready, help me set it up. Check the foreground app, recent activity, notifications and relevant permissions. Explain what you find, prefer reversible fixes, and ask before uninstalling apps or deleting data. Tell me what you couldn't verify.
```

## Security reports

The project ZIP was submitted for these checks:

- [SkillSecurity report](https://skillsecurity.net/r/01M7NJ1DD7KVGZHXE3R8ZJBHVY)
- [VirusTotal report](https://www.virustotal.com/gui/file-analysis/OTE2ZDlmNGIxMTM2N2E4NmIyNWU0M2RkMTI2ZjAxYWQ6MTc5NDk0NjIwNg==)

The submitted ZIP has this SHA-256:

```text
ca0682178cab4d150cef81dbeb3efd09525e06c88f110dc2cbc61d77a78dece8
```

The reports reflect the submitted ZIP and do not automatically cover later changes.

## Scope and privacy

This is a set of instructions for an AI agent, not an antivirus app. Android versions and manufacturers expose different diagnostics; a limited ADB check cannot prove a device is malware-free or prevent every future ad.

The skill does not require uploading device data. Diagnostic output can contain private information, so review it before sharing. You can inspect the complete instructions in [`SKILL.md`](skills/android-adware-check/SKILL.md).

---

Made with love by [Laflamme](https://github.com/lafllamme).
