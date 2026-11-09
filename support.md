---
layout: default
title: Sonic Sentinel Support
permalink: /support/
---

# Sonic Sentinel: Support

Sonic Sentinel is an acoustic burst watch for macOS and iOS. This page answers the common questions. If yours isn't here, get in touch through [danoli3.com](https://danoli3.com).

## Report a problem or ask for a feature

Open an issue at **[github.com/SonicSentinel/Support](https://github.com/SonicSentinel/Support/issues/new/choose)**: there are forms for bug reports, feature requests and questions. Issues there are **public** and handled by GitHub, not by the app, so please do not post recordings, private locations or your encryption salt. For anything private, get in touch through [danoli3.com](https://danoli3.com).

## Getting help

When you write, it helps to include:

- your macOS or iOS version, and the app version (on the **About** tab);
- the audio input you were using (built-in microphone, or the name of your interface) and its sample rate, which the app shows in the header as "up to … kHz";
- what you expected and what happened.

Exported reports contain detections (time, frequency, level) and never recorded audio, so they are safe to attach, but they are encrypted by default: decrypt one first if you want someone else to read it.

## Frequently asked questions

### The app can't hear anything, or says the microphone is not available

Sonic Sentinel needs permission to use the microphone.

- **macOS:** System Settings → Privacy & Security → Microphone, and switch Sonic Sentinel on.
- **iOS:** Settings → Sonic Sentinel → Microphone.

If you changed it while the app was running, restart the app. On iOS, Lockdown Mode can block external audio accessories until you approve them.

### Why don't I see any ultrasound?

The highest frequency an input can show is **half its sample rate**. At 48 kHz you only see up to 24 kHz. To see ultrasound you need an audio interface running at 96 kHz or 192 kHz, **and** a microphone that responds at those frequencies. Most built-in microphones do not capture anything above roughly 20 kHz. The header shows what your input can reach, and bands above it are marked as out of range.

### I see lots of "Ultrasound A" detections with my built-in microphone

If the band's learned floor is at the pipeline's own rounding noise (around -150 dBFS or lower), nothing real is being captured there. Short flat blips in such a band are tagged **INPUT ARTEFACT** and rated Info, so they do not raise alerts. A genuine tone in the same band is not tagged this way.

### How do I stop steady background noise from interfering?

Use **Calibrate room noise** on the Live tab with the input in its normal, quiet state. It learns about ten seconds of steady noise, and **Subtract room noise** then takes it out of the analysis. Anything steady that is present while you calibrate is learned as static and stops being reported, so calibrate in a known-clean state. Reports note when a profile was applied. See Settings → Room noise.

### What does a red alert mean?

A published acoustic signature was detected, for example two ultrasonic tones beating down to an audible one, an amplitude-modulated ultrasonic carrier, or an audible tone with a ripple. It means "look closer". Sonic Sentinel detects sound, it cannot identify a device or a person, and it cannot detect radio or microwave energy. It is not a medical or safety device.

### Notifications and alert sounds are not working

Both are **off by default**. Turn them on in Settings → Alerts. The app asks the system for permission the first time. If you refused, enable notifications for Sonic Sentinel in System Settings (macOS) or Settings (iOS).

### Where is my data, and how do I delete it?

Settings → Storage shows the folders. Everything is on your device and nothing is sent anywhere. To delete it, quit the app and delete the data folder, or delete the app on iOS. See the [privacy policy](/privacy/).

### I lost my encryption salt, or an encrypted file will not open

Settings, logs and reports are encrypted with a key made from your account name and a salt you control, kept in a file in the data folder or, if you chose, in the Keychain (Settings → Security). If the salt is lost, the encrypted files cannot be read: that is how the protection works. The app never overwrites settings it cannot read.

### The app feels slow

Turn on **Settings → Graphics → Show performance panel** to see the UI frame time and how much of real time the audio analysis takes. If you send a report about a slowdown, include what the panel shows.

## Contact

[danoli3.com](https://danoli3.com)
