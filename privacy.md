---
layout: default
title: Sonic Sentinel Privacy Policy
permalink: /privacy/
---

# Sonic Sentinel: Privacy Policy

**Effective date:** 10 November 2026
**App:** Sonic Sentinel (macOS and iOS), by Daniel Rosser
**Support:** [danoli3.com](https://danoli3.com)

## In short

- Sonic Sentinel **does not collect, transmit or share any personal data**. There are no accounts, no analytics, no advertising and no tracking.
- The app **makes no network connections of its own**. Nothing you hear, see or set in the app is sent to the developer or to anyone else.
- Audio from your microphone is **analysed on your device and is not recorded**.
- What the app keeps (your settings, and a log of detections) stays **on your device**, **encrypted by default**, and you can delete it at any time.

## What the app does with your microphone

Sonic Sentinel listens to the audio input you choose (the built-in microphone, a USB or Thunderbolt interface, or a loopback device) so it can show you the frequency content of the sound and tell you when something stands out, such as ultrasound, a loud tone or a sweep.

- The audio is processed as it arrives, in memory, to produce spectra, levels and detections. It is **not saved as audio** and is not sent anywhere.
- The app asks the operating system for permission to use the microphone. You can withdraw that permission at any time in System Settings (macOS) or Settings (iOS), and the app will stop listening.
- The app can also analyse a WAV recording that **you** select. That file is read on your device and is not copied or uploaded.

## What the app stores on your device

| What | Why | Where it lives |
|---|---|---|
| **Settings** (your choices, saved room-noise profiles) | So the app remembers how you set it up | The app's data folder, encrypted |
| **Detection log** (time, frequency, level, tags such as "ultrasonic burst" for each detection) | So you can review what was detected | The app's data folder, encrypted by default |
| **Exported reports** (JSON, Markdown, CSV), only when you export them | So you can read or share them yourself | The app's exports folder, encrypted by default |
| **Room-noise profile** (a spectrum of the steady background noise), only if you calibrate it | So steady noise can be subtracted from the analysis | Inside the encrypted settings |

None of this contains recorded audio. Reports and logs can include the **name of the input device** and **timestamps**, because that is part of describing a detection.

The exact folders are shown in **Settings > Storage** inside the app.

### Encryption

Settings, logs and exported reports are encrypted on your device (AES-256-GCM). The key is derived from your computer account name and a **salt** that you control. By default the salt is kept in a file in the app's data folder that only your account can read. You can choose to keep it in the **Keychain** instead (Settings > Security). The key and the salt never leave your device. If you lose the salt, encrypted files cannot be read: that is how the protection works.

## What the app does not do

- It does not connect to the internet by itself, and it contains **no analytics, advertising, tracking or crash-reporting libraries**.
- It does not collect your name, email address, location, contacts, photos or any identifier.
- It does not share anything with third parties, because it does not collect anything to share.

## Things you may choose to do

- **Notifications:** off by default. If you turn them on, the app asks the system for permission and shows **local** notifications on your device. Notifications are not sent through any server run by the developer.
- **Links:** the About page and the app's support link open **your web browser** when you click them. Once your browser opens a website, that website's own privacy policy applies. The app itself sends nothing.
- **Sharing reports:** exported reports are files on your device. If you send or upload one, you decide who receives it. Reports are encrypted by default, so decrypt a report (with the app) before giving it to someone who needs to read it.

## Apple and your device

If you opt in to sharing diagnostics with app developers in your device's settings, Apple may provide the developer with anonymous crash and usage statistics. That is controlled by Apple and your device settings, not by the app, and the developer cannot identify you from it. Apple's own [privacy policy](https://www.apple.com/legal/privacy/) governs the App Store and the operating system.

## Children

Sonic Sentinel is not directed at children and does not knowingly collect any information from anyone, including children.

## Deleting your data

Everything the app stores is in its data folder on your device. To delete it, quit the app and delete the folder shown in **Settings > Storage**, or delete the app (on iOS this removes its data). If you chose to keep the salt in the Keychain, remove the item named for Sonic Sentinel in Keychain Access, or switch off "Keep the salt in the Keychain" in Settings > Security first. The developer holds no copy, so there is nothing to request from the developer.

## Open-source components

The app is built with openFrameworks and other open-source libraries, listed on the app's **About** page with their licences. They run inside the app on your device and do not collect data.

## Changes to this policy

If the app's behaviour changes in a way that affects your privacy, this page will be updated and the effective date above changed before that version is released.

## Contact

Questions about this policy: [danoli3.com](https://danoli3.com)
