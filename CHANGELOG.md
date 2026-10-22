# Changelog

All notable changes to ElBee Player are listed here, newest first. Earlier releases are described on the
[GitHub releases page](https://github.com/ElBeeHQ/ElBeePlayer/releases).

## v0.12.01

A new look: an amber theme and a new app icon.

### Appearance

- **New app icon.** ElBee Player now has the Prism icon: three amber facets on a dark glass tile. It is also the logo on the
  launch, sign-in and About screens, and the playlist selector in the sidebar shows the prism with your connection status.
  The smallest sizes use a simplified version so they stay clear.
- **Amber accent.** Selection, focus, buttons, progress bars and highlights are now golden amber instead of violet.
- **Active rows glow softly.** The selected sidebar entry, category, playing channel and filter pill use a translucent amber
  fill with a thin amber border.
- **Neutral backgrounds.** The window backdrop and sidebar are plain grey glass without the blue and violet tint, and the
  sidebar icons are one crisp tone that turns amber when selected.
- **Tag pills.** Quality tags such as 4K, UHD and HEVC are now subtle translucent pills with a faint border.
- **Diagnostics overlay** has an amber hairline border.

## v0.11.02

Fixes updating to ElBee Player from inside the app. There are no other changes.

### Updating

- **Copies installed under the old name can now update.** The in-app updater could not install version 0.11.01 on a copy
  still called LiquidIPTV, and reported the update as improperly signed. That message was misleading: the updater picks the
  app to install by the installed app's file name, and the rename had changed it. Updates for those copies now carry the app
  under the name they expect. Your data comes across as described for 0.11.01.
- **The app may keep its old file name** in your Applications folder after updating (it still says ElBee Player inside).
  You can rename it to ElBee Player in Finder at any time. Later updates work either way.
- Version 0.11.01 can still be downloaded and installed by hand; it simply could not be installed by the updater.

## v0.11.01

LiquidIPTV is now **ElBee Player**. This release changes the name and how your data is stored, and adds one setting.
It is the same app: your playlists, settings and favourites come with you.

### A new name

- **ElBee Player** replaces the old name everywhere: the app (`ElBee Player.app`), Settings ▸ About, the licence and the
  notices. Downloads, updates and the issue tracker are at github.com/ElBeeHQ/ElBeePlayer. Copies you already have find this
  update at the same address as before.
- **Your data moves over automatically.** The first time it opens, ElBee Player brings across your settings, playlists,
  favourites, history, resume points, category choices, Series Link rules and downloads list from the previous version.
  macOS may ask for permission twice: once to read the previous version's data and once to use your saved passwords. Choose
  **Allow** or **Always Allow**; if you refuse, nothing is lost and it asks again next time.
- **Please re-choose your folders.** macOS ties permission to a folder to the app that was given it, so the **recordings
  folder** and the **downloads folder** must be chosen again in Settings ▸ Storage. Until then, recordings and downloads go
  to your Downloads folder. Reminders you had set in the TV Guide also need setting again, and macOS asks once more for
  permission to show notifications.

### Credentials and privacy

- **Server address, username and password are all kept in the macOS Keychain.** Before, only the password was; the
  address and username were in the app's preferences. Existing playlists are moved over once, and the old copies are deleted
  only after the new ones are saved.
- **Account details no longer appear in preference names or cache folder names.** Favourites, history, resume points and
  category choices are labelled with an anonymised identifier instead of "username@server", and are renamed for you.
- **The README now has Legal & Disclaimer and Privacy & Security sections.** ElBee Player is a media player that provides
  no content; you supply your own and are responsible for your right to view, record and download it. It collects no
  telemetry, analytics or personal data, and its only network connections are to your own IPTV service and to GitHub for
  updates.

### Sports

- **Custom Sports Keywords** (Settings ▸ Playback ▸ Streaming & Network). Add your own words, such as a broadcaster's
  name, to treat matching channels as sports channels for Sports Ultra-Low Latency Mode and for hiding spoilers. Only
  generic words (sport, football, soccer, golf, cricket, rugby, tennis and the like) are built in, so channels that are
  named only by a broadcaster need their name added here.

### Smaller changes

- Example text in Settings and the sign-in screen no longer names real broadcasters or programmes, and the server field's
  hint is now "Server address and port".
- The description of supported services now reads "IPTV services with an Xtream-style API".

## v0.10.02

A change to how ElBee Player is licensed and distributed. There are no changes to the app's features.

### Licence and downloads

- **ElBee Player is no longer published as open source.** The app remains available at no charge for personal, non-commercial
  purposes under a new licence (Settings ▸ About ▸ Licence). Versions up to and including 0.10.01 were released under the
  GNU General Public License, version 3, and anyone who received those keeps the rights that licence gave them.
- **Downloads and updates stay on GitHub** at github.com/ElBeeHQ/ElBeePlayer, which now holds the releases, the update
  feed and the issue tracker. Installed copies keep updating automatically from the same address.
- **Settings ▸ About** shows the new licence and a Downloads link in place of the source-code link, and the section for
  VLCKit and Sparkle is now called Third-Party Software. Their licences and notices are unchanged: VLCKit is still included
  unmodified as a separate framework that you can replace with your own build.

## v0.10.01

Data-saving controls for hotspots and travel, sharper video on Apple Silicon, a lower-latency profile and spoiler hiding
for sports, a quality menu for movies and series, and a reset button in Settings.

### Travel & Tethering Mode

- **General ▸ Network & Data:** **Travel & Tethering Mode** (Off, Auto-Detect Hotspots, Always On) and **Maximum Stream
  Quality** (Auto, 4K, 1080p, 720p, Standard Definition). With Auto, data saving uses 720p; a limit you choose, 4K included,
  is always respected. The limit applies to adaptive (HLS) streams that offer several qualities, from the next time a stream
  starts; single-quality and plain MPEG-TS streams have nothing to choose between.
- **Hotspot detection** reads macOS's own "expensive" and "constrained" flags, cellular links, and the address of the
  connection in use, because macOS is inconsistent about Wi-Fi and USB tethers: an iPhone's Personal Hotspot (Wi-Fi, USB or
  Bluetooth) and Android tethering are recognised.
- **Warning banner.** While a hotspot or metered connection is detected, a banner across the top of the main content says
  "Personal Hotspot connection detected. Data usage may be significantly higher. Review the stream quality options in
  Settings." **Settings…** opens Settings at Network & Data, and the close button hides it until the network drops and a
  hotspot is joined again. It shows whatever the mode is set to.

### Video upscaling (Apple Silicon)

- **Playback ▸ Video Rendering** (shown only on Apple Silicon Macs): **Video Upscaling** (Off, Auto, Always On) and **Upscale
  Sharpness** (0 to 100%, 50% by default). Auto leaves 4K channels alone. This sharpens the picture with VLC's video filter,
  not Apple's MetalFX, which VLC's player cannot use, so it uses more processor time; turn it off if playback stutters.

### Sports

- **Sports Ultra-Low Latency Mode** (Playback ▸ Streaming & Network, off by default) shrinks the buffer on sports channels
  and tries raw MPEG-TS before HLS, which runs closer to the live broadcast. It needs a stable connection and applies to the
  main player, not Multi-View. Sports channels are recognised by words in the channel or category name.
- **Hide EPG Spoilers for Sports** (off by default) blurs programme descriptions on sports channels in the Live TV player
  until you point at them, and leaves them out of the TV Guide tooltips.

### Movies and series: source and quality

- A **Source / Quality** menu beside Play and Download lists the other versions of a title (for example 4K, 1080p, 720p).
  Providers list each quality as its own entry, so entries are grouped by title once quality and codec words are removed.
  Choosing one opens that entry, so Play and Download act on it. Resume progress is kept per entry.

### Settings

- **Reset to Default Settings…** (General ▸ Reset) puts display, playback and behaviour settings back to their defaults after
  a confirmation. Playlists and sign-in, downloads, favourites, history, category choices, Series Link rules, the recordings
  and downloads folders, and the parental lock are not changed.
- The diagnostics overlay's Network line now measures real throughput on HLS streams, and the overlay shows in the floating
  window without crashing.

### Housekeeping

- The GitHub account is now **ElBeeHQ**: the source and issue links, the update feed and the release script use the new
  address. Copies already installed keep working because GitHub forwards the old address.
- Update notes shown in the update prompt are now formatted text, instead of escaped Markdown.

## v0.9.91

Three new power features (automatic recording by keyword, audio levelling and a stream diagnostics overlay), a new
Storage tab in Settings, and a round of visual polish on the channel and category lists.

### Series Link: automatic recording by keyword

- **Rules.** Add keywords such as "Football", "Evening News" or "Documentary"; any programme in the guide whose title
  contains one is recorded automatically. A rule can optionally be limited to channels whose name contains some text, which
  also keeps those channels' guides up to date. Manage them in **Library ▸ Auto-Record Rules…** (⇧⌘R), from the toolbar
  button in the TV Guide, by right-clicking a programme and choosing **Auto-Record "Title"**, or from Settings ▸ TV Guide.
- **Runs on its own.** Each recording uses a separate player with no picture or sound, so it never changes what you are
  watching. Files are saved to your recordings folder as `ElBeePlayer_Auto_<title>_<date>_<time>.ts`, with notifications when a
  recording starts, finishes or fails. The window lists what is scheduled and recent, with Cancel, Stop and Show in Finder.
- **Settings (TV Guide):** **Start Padding** (exact, 1, 2 or 5 minutes early), **End Padding** (exact, 2, 5 or 15 minutes
  late) and **Skip Duplicate Airings** (on by default), which skips a repeat of a programme already recorded or scheduled.
- **Settings (Storage):** **Auto-Delete Old Auto-Recordings** (never, 7, 14 or 30 days; files go to the Trash, and only
  Series Link's own files are touched) and **Storage Safety Threshold** (pauses recording below 5, 10 or 20 GB free).
- **Limits to know about.** Recording only happens while ElBee Player is open, and only for programmes in the guide it has
  loaded (favourites, channels you have watched, and channels named in a rule). At most two recordings run at once. Some
  providers allow only one connection per account, so a recording may fail, or interrupt what you are watching, while you
  stream on the same account; a notice says so in the rules window and in Settings.

### Audio normalisation and night mode

- **Audio Normalisation** evens out volume between programmes and ad breaks. **Dialogue Boost / Night Mode** compresses loud
  peaks so speech stays clear at low volume. Both are off by default, in Settings ▸ Playback ▸ Subtitles & Audio, apply to
  the player and Multi-View, and take effect the next time a stream starts.

### Stream diagnostics overlay

- **⌘I** (View ▸ Stream Diagnostics, with a checkmark while on) shows a translucent overlay on the picture: video codec,
  resolution, aspect ratio and frame rate; audio codec, channels and sample rate; network bitrate, buffer state and dropped
  frames. It works in the main player, the mini-player, full screen, the floating window and Multi-View (where it appears on
  every quadrant when that window has focus).
- **Settings ▸ Playback ▸ Player Controls:** **Show Diagnostics HUD on Stream Start**.
- The buffer line shows the stream's state and the cache size you configured, not a fill percentage, because libvlc does not
  report one.

### Settings

- **New Storage tab** holds the recordings and VOD download folders and the local cache, moved out of General, which is now
  shorter and easier to scan.
- **Combine Duplicate Categories** (General ▸ Channel Names, off by default) lists categories that differ only by quality
  tags (such as "UK| NEWS" and "UK| NEWS HEVC") as one. Locked categories are never combined.
- The Settings header is now a constant glass strip instead of a transparent one that text scrolled under, with no band
  appearing when the pointer moves over the tabs.

### Look and feel

- **Quieter tag chips.** A channel with UHD no longer also shows 3840P, chips are fainter, and the category list shows at
  most one chip per row (HD, RAW and similar are hidden). Rows that share a name keep their tags so they can be told apart.
- **Softer logo tiles** in dark mode, and a **clearer selected state** on the All / With Guide / Favourites filter.
- **Sidebar selection:** the system's blue highlight no longer draws over the violet selection in the sidebar, Library list
  and category list.
- **Live TV list:** the dividers, hover plate and playing-row plate now share the same edges, the playing channel's waveform
  icon is easier to see, and the list scrolls clear of the mini-player.

## v0.9.82

A polish pass on Settings, following a usability review of the v0.9.81 window.

### Settings: where things live

- **TV Guide now holds everything about the guide.** Highlight Catch-Up Channels and Compact Guide Rows (moved from
  Appearance) share a **Display** section. The rarely needed **Guide Time Offset** and the manual **Refresh Playlist &
  Guide Now** button sit in a collapsed **Troubleshooting** group. The button is renamed because it re-downloads the
  channel and title lists as well as the guide.
- **Fewer one-control sections.** Media Keys joined Player Controls, and the decoding engine moved into the collapsed
  Advanced Playback Settings. Multi-View's single Performance toggle joined **Layout**, and its audio options form
  **Audio & Focus**.
- **Channel Names (General)** replaces the "Data Parsing" heading and now links to **Manage Categories…**, so hiding,
  locking and ordering are no longer a surprise to find.
- **Per-tab window heights:** short tabs no longer sit in a tall empty window; General and the other long tabs scroll.

### Clearer wording and scope

- **Scope is stated.** Manage Categories names the playlist it is editing and says its changes apply to that playlist only;
  the guide's "Last Refreshed" names its playlist; the lock and category helper text says "per playlist".
- **Shorter, per-control helper text** replaces the long paragraphs that covered several controls at once.
- **Consistent labels:** "Enable …" prefixes are gone; bracketed "[Default]" and "[Recommended]" suffixes are replaced by
  plain wording in the helper text; the iCloud switch says what it syncs.
- **Disabled controls say why** (for example, Start Muted only applies when resuming a channel).

### Fewer dead ends

- A notifications-denied warning with an **Open Notification Settings** button appears under Reminders when macOS has
  notifications turned off for ElBee Player.
- **Manage Locked Categories…** is always available, with a note when the lock is off.
- The iCloud switch is hidden in builds that can't use iCloud, instead of being shown disabled.
- Folder rows are simpler: the path, a **Choose…** button and a menu (Show in Finder, Use Downloads), and the path
  controls now have VoiceOver labels.

### Fixes

- Removed a "BUG IN CLIENT OF KVS" message that was logged at launch in builds without the iCloud entitlement; the iCloud
  store is now only touched when sync is on and available.

## v0.9.81

The system-integration and polish release on the way to v1.0.0: a reorganised Settings window, a dedicated category
workspace, a quicker way to switch playlists, and the first set of native macOS integrations.

### Settings overhaul and reorganisation

- **A six-tab Settings window.** The window (680 × 560 pt) is rebuilt as grouped forms in the standard macOS style, with
  tabs for **General**, **Playback**, **TV Guide**, **Multi-View**, **Appearance** and **About**. It always opens on
  General.
  - **General:** Strip Country Prefixes; resume the last channel on launch and start muted; recordings and VOD download
    folders (with path controls, *Choose…*, *Use Downloads* and *Show in Finder*); a cache usage summary with *Clear Local
    Data Cache…* (confirmation sheet); software updates; Spotlight and iCloud switches; the parental lock.
  - **Playback:** skip interval (now 5, 10, 15 or 30 seconds), prevent display sleep, float video when minimised;
    subtitles by default, preferred subtitle language and a new **Default Audio Track** language; media keys; the
    decoding engine; and a collapsed *Advanced Playback Settings* group holding buffer caching, deinterlacing and the
    deinterlace mode.
  - **TV Guide:** automatic refresh (new **Every 6 Hours** option), EPG time offset, a *Force Refresh EPG Now* button with
    the last-refreshed time, reminder lead time and sound, and a switch for highlighting catch-up channels.
  - **Multi-View:** default layout, mute non-focused quadrants, highlight the active border, and stop decoding on hidden
    quadrants.
  - **Appearance:** keep the window on top, Liquid Glass vibrancy with *Reset to Default*, show channel logos in lists, and
    compact EPG cells.
  - **About:** now also shows the build number.
- **Category management moved out of Settings** into its own **Manage Categories** window: *Library ▸ Manage Categories…*
  (⇧⌘K), a new button in the sidebar footer, or *Manage Locked Categories…* in Settings. It keeps everything from before:
  visibility checkboxes, drag-and-drop ordering, the Hide Non-English rule, per-channel hiding and the channel reorder
  sheet, and adds a lock control per category.
- **Nothing is reset.** Every existing preference keeps its stored key and value (`resumeLastChannelOnLaunch`,
  `startMuted`, `skipIntervalSeconds`, `subtitlesOnByDefault`, `preferredSubtitleLanguage`, `alwaysOnTop`, `glassVibrancy`,
  `stripCountryPrefixes`, `preventDisplaySleep`, `hardwareDecoding`, `networkCachingMs`, `epgOffsetHours`,
  `epgRefreshInterval`), and saved category preferences still load. Only additions are new.
- The Multi-View layout is now a Settings default for newly opened windows. The window's own toolbar toggle still switches
  it for the session, and the layout key saved by v0.9.71 is no longer read.

### Sidebar and playlist quick-switcher

- **A dedicated, full-width playlist row** sits at the foot of the sidebar above the Manage Categories and Settings
  buttons, so the playlist name has room and no longer truncates beside the icons.
- **A native quick-switch menu.** Clicking the row opens a standard pull-down menu: every saved playlist, a checkmark on the
  active one, and **Manage Playlists…** below a separator for the full manager (expiry dates, connection limits, Add
  Playlist). Choosing a playlist switches to it at once, with no extra window.
- **Connection status dots.** Each playlist has a green, orange or red dot. The active playlist shows its live state:
  green when signed in and reachable, orange while signing in, switching, loading the library or refreshing the guide, and
  red when offline, when the library fails to load, or when sign-in fails. The other playlists are checked with a quick
  login (8-second limit) each time the menu opens, and show grey until checked.

### Native macOS system integrations

- **Spotlight.** With *Index Content in macOS Spotlight* on, favourites, then live channels, movies and series (up to
  30,000 items, in batches) are registered with Core Spotlight, and choosing a result in Cmd + Space starts it in
  ElBee Player. Turning the switch off removes everything again.
- **Media keys and Control Centre.** What is playing (title, episode, artwork, position and play state) is published to
  Control Centre, and the Mac's Play/Pause, Skip and Next keys control the player. It can be switched off in Settings ▸
  Playback.
- **Parental lock.** Categories can be locked in Manage Categories. Opening one, or playing a channel from it (including
  from Favourites, search, Spotlight, Multi-View and the TV Guide), needs Touch ID or the Mac's account password, checked
  by the system; ElBee Player never sees the password. Locked categories show a lock in the category list, and stay open for
  the rest of the session once unlocked. Turning the lock on or off also asks.
- **iCloud state sync.** Favourites and Continue Watching positions are wired to `NSUbiquitousKeyValueStore`: the newer
  favourites list wins, and for each title the most recent position wins. **This needs a build signed by an Apple Developer
  team with iCloud enabled; this build is not, so the switch is shown as unavailable and nothing is uploaded.**

### Power features and enhancements

- **Reminder lead time.** TV Guide reminders can fire at the start of the programme or 2, 5 (default) or 15 minutes
  before, with or without a sound. The notification text follows the chosen lead time. Reminders already set keep the lead
  time they were created with.
- **Offline VOD downloads.** Movie pages have a **Download** button and each episode a download icon, saving the title's own
  file to the downloads folder from Settings, using a background URL session so it carries on while the app is busy.
  Progress shows beside the button, with cancel, then *Downloaded* with Show in Finder and Remove. A downloaded title plays
  from the file on the Mac.
- **Default audio track.** When a stream offers several audio tracks, the one in your preferred language is selected
  automatically.
- **Guide display options.** Compact EPG cells shorten the TV Guide rows, the catch-up icons can be hidden, and channel
  logos can be hidden in lists.
- **Multi-View options.** Quadrants can stay audible, the active border can be turned off, and hidden quadrants can keep
  running when the layout is reduced.

### Notes and known limitations

- iCloud sync is unavailable until the app is signed with an iCloud-enabled developer team (see above).
- Parental-lock unlocks last for the current session only.
- A Spotlight result that launches the app from scratch may be missed while the library is still loading.
- The status dots of non-active playlists are checked only when the playlist menu opens, and a provider that refuses a
  second simultaneous login can show red for a playlist that works when switched to.
- The status dot in the playlist button no longer pulses while connecting (a native pull-down cannot animate it).
