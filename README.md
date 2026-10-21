# Mithras 2 releases

Installer downloads and the update feed for **Mithras 2**, a Windows chat app for Claude built with
[Tauri 2](https://v2.tauri.app).

This repository holds **only releases**. The source lives in the private `Fleski/mithras2` repository; its release
workflow uploads each version here so installed apps can check for updates without a login.

## Install

Download `Mithras-2-Setup-<version>.exe` from the latest release and run it. The installer is per-user, needs no
administrator rights, and is **not code-signed**: Windows SmartScreen will show "Windows protected your PC" the first
time. Choose *More info* → *Run anyway*.

The app holds no API key. Credentials reach a machine once, through `hdh setup` in a terminal: the installer puts
`hdh.exe` beside the app, and Settings shows the command to copy.

## Update

Installed apps check this repository's latest release about 15 seconds after they start, every 6 hours after that,
and on demand (Settings → Updates → *Check now*). Each release carries three files that the updater needs and that
must keep their names: the installer, its `.sig` and `latest.json`. Draft and pre-release entries are invisible to
installed apps.
