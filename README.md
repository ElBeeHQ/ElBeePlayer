<p align="center">
  <img src="assets/icon.png" alt="ElBee Player icon" width="128" height="128">
</p>

<h1 align="center">ElBee Player</h1>

<p align="center">
  <strong>A fast, native IPTV player for the Mac.</strong><br>
  Live TV, a full TV Guide, movies, series and radio, built from the ground up with SwiftUI.
</p>

<p align="center">
  <a href="https://github.com/ElBeeHQ/ElBeePlayer/releases/latest"><strong>Download the latest release</strong></a>
  &nbsp;·&nbsp;
  <a href="CHANGELOG.md">What's new</a>
  &nbsp;·&nbsp;
  <a href="https://github.com/ElBeeHQ/ElBeePlayer/issues">Report a problem</a>
</p>

<p align="center">
  Free for personal use · macOS 15 or later · Apple Silicon and Intel · Updates itself
</p>

---

ElBee Player works with IPTV services that offer an Xtream-style API. Sign in with your provider's server address,
username and password, and your channels, programme guide, movies and series are ready in moments. A short setup guide
then helps you choose your languages, categories and preferences. Every visit after that opens straight from a cache on
your Mac.

> **ElBee Player is a player only.** It comes with no channels, playlists or content of any kind. You bring your own
> service. See [Legal & Disclaimer](#legal--disclaimer).

## Highlights

### A home screen made for you

- **Home** opens on a banner of new releases with backdrops, plots and one-click Play or More Info. It runs edge to
  edge, under the toolbar and the sidebar.
- **Continue Watching** picks up exactly where you left off, and **On Now** tiles show what's on your favourite
  channels, how far through it is and what's next.
- **Recommended for You** and **Because You Watched** are worked out on your Mac from what you watch, favourite and
  finish. Each one says why it was chosen. Nothing leaves your Mac.
- **Arrange Home** to reorder its sections or switch any off, and choose which screen the app opens on.

### Now Playing

- **Live channels, movies and episodes** all open on one Now Playing page. Live TV shows the programme guide below the
  picture. Movies show their details, cast and director. Episodes show their plot and the episodes up next.
- **Up Next appears as the credits roll.** ElBee Player spots the end credits in the picture itself and starts a
  6-second countdown, with **Play Now** and **Keep Watching**.
- **← / → to skip and Space to pause**, with a "+10s" pill, just as in full screen, without bringing up the controls.
- **Subtitles** from the player itself: switch them on or off, choose the language and pick a size (Small to Extra
  Large) that changes at once, without restarting the stream. While they're on, the controls sit below the picture so
  they never cover them. Subtitles a channel sends as pictures keep the channel's own size.
- **Subtitle timing:** if a channel's subtitles run ahead of the dialogue or behind it, move them earlier or later in
  half-second steps (⌘[ and ⌘]). The timing is remembered for each channel, film and episode.
- **Live Captions** (experimental, macOS 26): your Mac writes captions for live channels that have no subtitles, from
  the channel's sound, on your Mac. They build up word by word on two lines that roll up, so what you've read stays
  put. Only one of captions and subtitles shows at a time.
- **Full screen in one smooth move:** the picture grows to fill the screen and shrinks back, with the menu bar and Dock
  hidden and no slide to a new Space. **Use Full-Screen Spaces** (Settings > Playback) gives it a Space of its own.
- **A movie or episode on its own page:** press Back while one plays and the picture moves to the top of its page,
  above the details, with the usual controls. Browse anywhere else and it carries on in the mini player.
- **Mute stays on** for whatever you play next, until you unmute or quit.
- **The picture glides** between Now Playing, the Live TV and Guide banners and the mini player, and keeps playing as it
  moves, with no pause (**Smooth Picture Moves**, on by default in Settings > Playback). ElBee Player draws each frame
  itself, with hardware decoding: colours follow each stream's own colour settings, and subtitles stay on hardware
  decoding, so they cost little energy, 4K included.
- **HDR:** HDR10 and HLG streams play in 10-bit and show in HDR, brighter than white, on displays that support it.
- **The same controls in every player:** the mini player, the floating window, the banners, Now Playing and full screen
  share one set of buttons, with Full Screen always last. A glass **close cross** appears when you point at the picture and ends the video.
- **Cast to a TV or speaker:** the Cast button in every player lists the TVs and speakers on your network. Pick one and
  what's playing carries on there from the same spot, with Play/Pause, the skips and the progress bar still working.
  **Stop Casting** brings it back to your Mac. **Cast Quality** in Settings › Playback sets how hard your Mac works when
  a device can't play a stream as it is.
- **Reconnecting… is shown, not hidden:** if a stream drops, a pill over the picture says so while the app tries again.
- **A clean mini player:** just the picture, with its controls over it when you point at it.
- **One click** on a banner's picture opens Now Playing.

### Advanced Video

- **Ambient Glow** surrounds the picture with soft light in the colours at its edges, about twelve times a second,
  and costs little energy: it redraws only when its colours change. Widescreen films keep their glow, taken from the
  picture inside their black bars (with Smooth Picture Moves the bars are trimmed and the glow fills them). It
  changes with a scene at once and stays steady otherwise. In full screen it softly fills the black bars, and on Now
  Playing it spreads into the page around the picture. It also lights the Live TV and Guide banners. In Dark Mode it glows. In Light Mode it gently tints the page,
  and dark scenes cast a soft shadow instead.
- **Match Frame Rate** switches your display to a refresh rate that fits the stream in full screen, such as 50 Hz for
  25 or 50 fps or 59.94 Hz for 29.97, so pans don't judder. Your display goes back as it was afterwards.
- **Deinterlacing:** Auto, Yadif, **Yadif 2x** (smooth 50 full frames a second from 50i sport) and Blend. Changes apply
  to the stream already playing. Auto treats only live channels marked as interlaced, and 4K is never deinterlaced.
- **Sharpening** makes lower-resolution channels crisper on Apple Silicon. **Decoding options**, subtitles and audio
  tracks are all there too.
- Everything is in one **Advanced Video** menu in the player, and in Settings › Playback.

### Live TV

- **Channel spotlight:** click a channel and it fills a banner at the top: what's on, how far through it is, what's
  next, and Watch, Record and Favourite. Double-click to play straight away, or move through the list with ↑ / ↓ and
  press Return.
- **Live preview:** the channel you click plays right in the banner. It uses your one stream (most providers allow
  only one), waits a moment as you click down the list, and holds back while you're recording, watching a movie or
  episode, or using Multi-View. Click **Muted** for sound, point at the picture for Mute, Expand to Now Playing and Full
  Screen, or double-click it to open Now Playing. It stays in the banner as you browse other categories.
- **One row per channel:** HD, 4K, +1 and other versions of a channel share a row, with a button to play each one, or
  right-click for the list, with the sharpest picture marked.
- **Now and next in every row**, with sorting by number or name, and a find box for the category.
- **Categories grouped by country** in the sidebar, under headings you can fold away.

### TV Guide

- **A scrolling guide** you can drag around with the mouse. Channel names stay in view as you scroll through time.
- **Programme spotlight:** click a programme to see its details. If it's on now, watch it, with the live preview. If
  it's later, set a **reminder** or a Series Link. If it has finished, watch it from catch-up.
- **Day buttons** from catch-up days to a week ahead, a **Now** button, and All / Favourites / Catch-Up filters.
- **A calm grid:** a thin progress bar on what's on now, earlier programmes dimmed, bells only where a reminder is set,
  and an amber line marking the time.

### Radio

- **Station tiles** coloured by genre, with **genre buttons** to narrow them and your **Recently Played** stations.
- **Now Playing banner** for the station you're listening to, with Pause, Favourite and volume. Tiles play without
  leaving the page.

### Multi-View, catch-up and sport

- **Multi-View** plays up to four channels at once, each fully independent (⇧⌘M).
- **Catch-up TV** where your provider offers it.
- **Sports mode:** a low-latency profile that runs closer to the live broadcast, plus optional **spoiler hiding** for
  programme descriptions on sports channels.
- **Instant resume:** the app opens quietly on your last channel.

### Record and download

- **Record live channels** with one click, or set up **Series Link** to record programmes automatically by keyword.
  It adds padding before and after, skips repeats and protects your free disk space (⇧⌘R).
- **Download movies and episodes** to watch offline.
- Recordings and downloads go to a folder you choose.

### Movies and series

- **Rich detail pages** with fanart backdrops, ratings, age ratings, cast and director, trailers, and a **You May Also
  Like** shelf.
- **One season at a time**, with episode stills, air dates and running times.
- **A source and quality menu** when a title comes in several versions.
- **Resume points, favourites, history and ratings** across the whole library.

### Your library, your way

- **Content Languages:** tick the languages you want, and only categories, channels and titles in those languages show,
  everywhere in the app.
- **Hide provider tags** such as "TOP - " or "4K - " in titles.
- **Manage Categories** to reorder, hide or lock categories and their channels (⇧⌘K).
- **Several playlists**, switched from the sidebar, with the catalogue refreshing quietly in the background. The app
  opens on a **playlist chooser** showing each server's status (⌘1 to ⌘9 to sign in), or straight into the playlist
  you choose in Settings › General › Startup. File › Choose Playlist… (⇧⌘P) goes back to it.
- **A parental lock** that asks for Touch ID, an Apple Watch or your Mac's password before a locked category opens.
  The system does the checking, and ElBee Player never sees your password. Unlocked categories can lock again after a
  set time, and locked ones can be hidden altogether.

### Feels at home on the Mac

- **The system's own glass** for the toolbar, player controls, mini player and pop-ups on macOS 26.
- **Plain Look** (Settings > Appearance) swaps the system glass for a plainer look, if you prefer it.
- **Light, Dark or Automatic** for ElBee Player alone, from the sun and moon button by the Settings gear.
- **Interface Size** makes text larger throughout the app on a big or high-resolution display.
- **Spotlight search**, **media keys** and **Control Centre** playback controls.
- **Quiet launch:** optionally resume the last channel, muted if you like. A channel that can't be reached, or that is
  only sending black, is dropped silently, so you never land on an empty box.
- **Keychain and the sandbox:** your sign-in is kept in the macOS Keychain, and the app runs in the App Sandbox.
- **iCloud sync** (optional) shares favourites and Continue Watching between your Macs.
- **Hover feedback everywhere:** toolbar tabs, guide programmes and channel rows light up softly under the pointer.
- **Stream diagnostics** overlay (⌘I), **audio normalisation** and a **night mode** for quieter evenings.
- **Data Saver** spots a phone hotspot and limits stream quality, so you don't use up your data.
- **Glass over the picture:** every control, badge and banner over a video sits on the same glass.
- **Every setting explains exactly what it does**, grouped so you can find it quickly, and **Search Settings** (⌘F in
  Settings) finds any of them by name or by the words you'd use. Each page has its own Restore Defaults.

## Install

1. Download `ElBeePlayer-x.y.z.zip` from the [latest release](https://github.com/ElBeeHQ/ElBeePlayer/releases/latest).
2. Unzip it and drag **ElBee Player** into your Applications folder.
3. The app is not notarised by Apple, so the first time you open it macOS may say it cannot verify it. Open
   **System Settings → Privacy & Security**, scroll to the message about ElBee Player and click **Open Anyway**.
   If macOS says the app is "damaged", run this once in Terminal and open it again:
   ```bash
   xattr -dr com.apple.quarantine "/Applications/ElBee Player.app"
   ```
4. Sign in with your provider's server address, username and password.

**Requirements:** macOS 15 or later, on Apple Silicon or Intel. The system glass look needs macOS 26, and
Sharpening needs Apple Silicon. Everything else works on every supported Mac.

## Updates

ElBee Player updates itself. Open **Settings → General → Software Updates** and choose **Check for Updates Now…**, or
leave automatic checks on. Updates are downloaded from this repository and checked against ElBee Player's signing key
before they're installed. Then the app restarts. Your playlists, favourites and settings are kept.

See the [changelog](CHANGELOG.md) for what changed in each release.

## Keyboard shortcuts

| Shortcut | Action |
| --- | --- |
| Space | Play or pause |
| ← / → | Skip back or forward |
| ↑ / ↓, Return | Move the Live TV spotlight, then play |
| ⌘F | Search |
| ⌘I | Stream diagnostics |
| ⌘[ / ⌘] | Subtitles earlier or later |
| ⇧⌘M | Multi-View |
| ⇧⌘K | Manage Categories |
| ⇧⌘R | Series Link (auto-record rules) |
| ⇧⌘P | Choose Playlist |

## Privacy & Security

- **All user credentials, including server addresses, usernames, and passwords, are stored securely within the
  encrypted macOS Keychain.** None of it is sent to the developer.
- **No telemetry, analytics, accounts, advertising or tracking.** ElBee Player does not send what you watch, your
  playlists, your favourites or your settings to the developer or to any third party. Recommendations and credits
  detection run entirely on your Mac.
- **The only network connections it makes** are to the IPTV service you enter (channel lists, programme guide, the
  artwork addresses the service supplies, and the streams themselves) and to GitHub, to check for and download updates.
  When you cast, it also finds TVs and speakers on your local network and sends the stream to the one you pick; macOS
  asks your permission for that the first time.
  You can turn automatic update checks off in Settings → General → Software Updates. As with any web request, GitHub can
  see your IP address and the app version.
- **Local data** (cached channel lists, guide and artwork, favourites, history and settings) stays on your Mac, inside the
  app's sandbox, and is labelled with an anonymised identifier rather than your server address or username. You can
  clear the caches in Settings → Storage.
- **App Sandbox:** the app runs in the macOS App Sandbox. It can reach the network and the folders you choose for
  recordings and downloads (Downloads by default), and nothing else.

## Legal & Disclaimer

**This application is a media player and provides zero content, playlists, or channels. Users must provide their own content.**

**Users are solely responsible for ensuring they have the legal right to view, record, and download any media they supply to the application.**

- ElBee Player does not include, host, sell, recommend or link to any channels, playlists, programme listings or IPTV
  services, and it ships with no example providers.
- It contains no tools to bypass encryption, copy protection or access controls.
- Recording and downloading are for your personal use of content you have the right to record or download.
- ElBee Player is not affiliated with or endorsed by any broadcaster, content owner, IPTV service, VideoLAN, Apple or
  Sparkle. All names and trademarks belong to their respective owners.

## Support

Found a problem or have an idea? Open an [issue](https://github.com/ElBeeHQ/ElBeePlayer/issues).

## Licence

Copyright (c) 2026 ElBeeHQ. All rights reserved. The app is available at no charge for personal, non-commercial
use; see [`LICENSE`](LICENSE). Versions up to and including 0.10.01 were released under the GNU General Public
License, version 3.

## Third-party software

ElBee Player uses [VLCKit](https://code.videolan.org/videolan/VLCKit) (LGPL 2.1 or later) and
[Sparkle](https://github.com/sparkle-project/Sparkle) (MIT). Their licences and the full notices are in
[`licenses/`](licenses/) and under **Settings → About** in the app. VLCKit is included unmodified as a separate
framework inside the app, so you can replace it with your own build.
