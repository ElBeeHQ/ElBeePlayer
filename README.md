# LiquidIPTV

A native macOS IPTV player for Xtream Codes providers, built with SwiftUI.

LiquidIPTV is an independent player. It does not provide any channels, films or programmes; it plays what your own
IPTV provider supplies, and you are responsible for having the right to access that content.

This repository hosts the downloads and the update feed for LiquidIPTV.

## Features

- Live TV, a scrolling TV Guide with reminders, Movies, Series and Radio
- Several playlists, instant launch from a cache, and a silent resume of your last channel
- Favourites, watch history, resume points, ratings and details
- Mini-player, full screen, Multi-View (up to four channels), subtitles, deinterlacing and decoding options
- Series Link: record programmes automatically by keyword, with padding, repeat-skipping and disk safeguards
- Recording of live channels, offline VOD downloads, and catch-up TV where your provider offers it
- Audio normalisation and night mode, a stream diagnostics overlay (⌘I), and optional video sharpening on Apple Silicon
- Sports low-latency mode and spoiler hiding, a source / quality menu for movies and series
- Travel & Tethering Mode, which limits stream quality on a phone hotspot
- Spotlight search, media keys and Control Centre, a parental lock, and automatic updates

## Install

1. Download `LiquidIPTV-x.y.z.zip` from the [latest release](https://github.com/ElBeeHQ/LiquidIPTV/releases/latest).
2. Unzip it and drag **LiquidIPTV** into your Applications folder.
3. The app is not notarised by Apple, so the first time macOS may say it cannot verify it. Open
   **System Settings → Privacy & Security**, scroll to the message about LiquidIPTV and click **Open Anyway**.
   If macOS says the app is "damaged", run this once in Terminal and open it again:
   ```bash
   xattr -dr com.apple.quarantine /Applications/LiquidIPTV.app
   ```
4. Sign in with your provider's server address, username and password.

Requires macOS 15 or later (Apple Silicon or Intel).

## Updates

Open **Settings → General → Software Updates** and choose **Check for Updates Now…**, or leave automatic checks on.
Updates are downloaded from this repository, checked against LiquidIPTV's signing key, installed for you, and the app
restarts. Your playlists, favourites and settings are kept.

## Support

Open an [issue](https://github.com/ElBeeHQ/LiquidIPTV/issues) to report a problem or ask for a feature.

## Licence

Copyright (c) 2026 ElBeeHQ. All rights reserved. LiquidIPTV is free to download and use for personal, non-commercial
purposes; see [`LICENSE`](LICENSE). Versions up to and including 0.10.01 were released under the GNU General Public
License, version 3.

## Third-party software

LiquidIPTV uses [VLCKit](https://code.videolan.org/videolan/VLCKit) (LGPL 2.1 or later) and
[Sparkle](https://github.com/sparkle-project/Sparkle) (MIT). Their licences and the full notices are in
[`licenses/`](licenses/) and under **Settings → About** in the app. VLCKit is included unmodified as a separate
framework inside the app, so you can replace it with your own build.
