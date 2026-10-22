<p align="center">
  <img src="assets/icon.png" alt="ElBee Player icon" width="128" height="128">
</p>

<h1 align="center">ElBee Player</h1>

A native macOS IPTV player for IPTV services with an Xtream-style API, built with SwiftUI.

This repository hosts the downloads and the update feed for ElBee Player.

## Legal & Disclaimer

**This application is a media player and provides zero content, playlists, or channels. Users must provide their own content.**

**Users are solely responsible for ensuring they have the legal right to view, record, and download any media they supply to the application.**

- ElBee Player does not include, host, sell, recommend or link to any channels, playlists, programme listings or IPTV
  services, and it ships with no example providers.
- It contains no tools to bypass encryption, copy protection or access controls.
- Recording and downloading are for your personal use of content you have the right to record or download.
- ElBee Player is not affiliated with or endorsed by any broadcaster, content owner, IPTV service, VideoLAN, Apple or
  Sparkle. All names and trademarks belong to their respective owners.

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

1. Download `ElBeePlayer-x.y.z.zip` from the [latest release](https://github.com/ElBeeHQ/ElBeePlayer/releases/latest).
2. Unzip it and drag **ElBee Player** into your Applications folder.
3. The app is not notarised by Apple, so the first time macOS may say it cannot verify it. Open
   **System Settings → Privacy & Security**, scroll to the message about ElBee Player and click **Open Anyway**.
   If macOS says the app is "damaged", run this once in Terminal and open it again:
   ```bash
   xattr -dr com.apple.quarantine "/Applications/ElBee Player.app"
   ```
4. Sign in with your provider's server address, username and password.

Requires macOS 15 or later (Apple Silicon or Intel).

## Updates

Open **Settings → General → Software Updates** and choose **Check for Updates Now…**, or leave automatic checks on.
Updates are downloaded from this repository, checked against ElBee Player's signing key, installed for you, and the app
restarts. Your playlists, favourites and settings are kept.

## Privacy & Security

- **All user credentials, including server addresses, usernames, and passwords, are stored securely within the
  encrypted macOS Keychain.** None of it is sent to the developer.
- **No telemetry, analytics, accounts, advertising or tracking.** ElBee Player does not send what you watch, your
  playlists, your favourites or your settings to the developer or to any third party.
- **The only network connections it makes** are to the IPTV service you enter (channel lists, programme guide, the
  artwork addresses the service supplies, and the streams themselves) and to GitHub, to check for and download updates.
  You can turn automatic update checks off in Settings → General → Software Updates. As with any web request, GitHub can
  see your IP address and the app version.
- **Local data** (cached channel lists, guide and artwork, favourites, history and settings) stays on your Mac, inside the
  app's sandbox, and is labelled with an anonymised identifier rather than your server address or username. You can
  clear the caches in Settings → Storage.
- **App Sandbox:** the app runs in the macOS App Sandbox. It can reach the network and the folders you choose for
  recordings and downloads (Downloads by default), and nothing else.

## Support

Open an [issue](https://github.com/ElBeeHQ/ElBeePlayer/issues) to report a problem or ask for a feature.

## Licence

Copyright (c) 2026 ElBeeHQ. All rights reserved. The app is available at no charge for personal, non-commercial
use; see [`LICENSE`](LICENSE). Versions up to and including 0.10.01 were released under the GNU General Public
License, version 3.

## Third-party software

ElBee Player uses [VLCKit](https://code.videolan.org/videolan/VLCKit) (LGPL 2.1 or later) and
[Sparkle](https://github.com/sparkle-project/Sparkle) (MIT). Their licences and the full notices are in
[`licenses/`](licenses/) and under **Settings → About** in the app. VLCKit is included unmodified as a separate
framework inside the app, so you can replace it with your own build.
