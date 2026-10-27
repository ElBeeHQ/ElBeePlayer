# Changelog

All notable changes to ElBee Player are listed here, newest first. Earlier releases are described on the
[GitHub releases page](https://github.com/ElBeeHQ/ElBeePlayer/releases).

## v0.26.01: M3U playlists

M3U playlists join Xtream Codes accounts, Manage Playlists is redesigned with backup addresses for each account, and ElBee Player now installs from a disk image.

### New

- **M3U playlists:** add a playlist from a web address or a file on your Mac, alongside Xtream Codes accounts (**Manage Playlists › Add Playlist**, or the sign-in screen). Its TV guide comes from the address the playlist names, or one you enter.
- **Backup addresses:** give an account other addresses for the same service. They're tried in order when the main server doesn't answer, each shows whether it's working, and the playlist list warns when one stops responding.
- **Install window:** ElBee Player now downloads as a disk image. Opening it shows the app beside your Applications folder, ready to drag across. Copies already installed keep updating from inside the app as before.

### Improved

- **Manage Playlists:** redesigned, with every playlist in a sidebar showing its status and library size, a larger **Add Playlist** button, tidier details, and nothing to scroll past to save. Drag playlists to reorder them; editing a playlist's server or username keeps its favourites and history.

### Fixes

- **Banners:** a faint dark line no longer runs half way across the banner on Home, Live TV and the TV Guide, and the picture's glow now spreads smoothly behind the text.

## v0.25.02: elbeehq.com

ElBee Player has a website: elbeehq.com, with downloads, the notes for every release, an install guide and support.

### New

- **elbeehq.com:** download the latest version, read What's New for every release, and find an install guide, answers to common questions, keyboard shortcuts and a way to contact us.
- **Linked from the app:** the website sits at the foot of the sign-in, playlist chooser and loading screens, in **About ElBee Player**, in **Settings › About** and at the bottom of the **What's New** panel. The update window links to it under the notes.
- **Help menu:** **ElBee Player Website**, **Release Notes** and **Report a Problem**, in place of a Help item that had nothing to open.
- **Settings › About:** a **Website** row, **Legal & Terms** beside the licence, and **Report a Problem** under **Support**.

## v0.25.01: Playback options, Pin to Home, What's New

More control while you watch, a What's New panel after each update, and your favourite categories pinned to Home.

### While you watch

- **Playback options:** a new **⋯** button in every player, and a new **Playback** menu in the menu bar, hold the five
  options below. A short note over the picture confirms each change.
- **Sound timing:** if the sound runs ahead of the picture or behind it, move it earlier or later in 0.05-second steps
  (⌥⌘[ and ⌥⌘]). The timing is remembered for each channel, film and episode.
- **Playback speed:** watch movies and episodes from 0.5× to 2× (⌥⌘← and ⌥⌘→). The speed carries on to the next title
  until you quit. Live channels always play at normal speed.
- **Previous Channel (⌘L)** goes back to the channel you were watching before, in the same player.
- **Sleep timer:** stop playback after 15 minutes to 2 hours, at the end of the programme, or at the end of the movie
  or episode (before the next one starts). The sound fades out over a few seconds first.
- **Save Still (⌥⌘S)** saves the picture on screen as a full-size image in your recordings folder.

### New

- **What's New:** after an update, once ElBee Player has signed back in to your playlist, a panel over the library shows what changed in every version since the one you last used, newest first. Press **Continue** (or Return or Escape) to carry on. **Help › What's New in ElBee Player** shows the current version's notes again at any time. The notes come with the app, so they need no connection.
- **Every update in the update window:** when you skip a few updates, the update window now lists the changes in each version since yours, not only the newest.
- **Pin categories to Home:** right-click a category in Live TV, the TV Guide, Radio, Movies or Series and choose **Pin to Home**. It appears under **Pinned** in the Home sidebar, one click from opening it. Drag pins to reorder them, and right-click one to unpin it. **Reset Category Choices** clears pins too.

### Fixes

- **Live Captions with sound timing or speed:** with Live Captions on, a changed speed or a saved sound timing now
  stays in step with the picture straight away, instead of until the next skip.
- **Mini-player after Now Playing:** going from Now Playing back to Home no longer leaves the mini-player empty a moment after the picture lands in it.

## v0.24.02: Sharpening, subscription reminder, download progress, lighter Live TV and Guide

Sharpening that works, a subscription reminder, download progress bars, a TV Guide that opens where you need it, and far less energy on Live TV and the Guide.

### New

- **Subscription reminder:** when your playlist's subscription runs out within 7 days, a note above the playlist switcher says when. Close it and it stays away for the rest of the day, for that playlist. The date is checked again with your provider when you come back to the app or wake your Mac.
- **Download progress:** a movie or series being downloaded shows a progress bar under its title, with the size and time left, and **Cancel** on the movie's page. A series adds up all its episodes, and each downloading episode has a small bar of its own in its row.
- **Movies and episodes open in Now Playing**, like live channels. Full screen is one click away.

### Video

- **Sharpening works:** it had made no difference to the picture. It now sharpens on your Mac's graphics chip, with both renderers, alongside deinterlacing and subtitles, and you can see the difference between 0% and 100%. Auto still leaves 4K alone.
- **Ambient Glow follows the picture:** in the Live TV and Guide banners it now takes new light at once, so cuts show straight away, and holds steady through compression noise in a still scene.
- **Even light round the picture:** a thin strip of glow no longer fades to nothing at its ends (the dark gap above a banner's picture), and the light is read from just inside the picture, past the dark lines some streams have at their edges.
- **Blues in Light Mode:** a vivid blue picture now tints the page blue instead of casting a grey shadow.

### TV Guide

- **Opens on the half hour before now,** so the now line sits a little way in and what's on now shows from its start. **Now** jumps to the same place.
- **Titles stay in view:** a programme that started before the visible part of the guide shows its title and times from the edge you can see.

### Lighter on your Mac

- **Live TV and the TV Guide:** with a channel in the banner and nothing else happening, ElBee Player went from more than 1,000 Energy Impact to about 60–90 on a test Mac. The banner's backdrop carries over between Live TV and the Guide without starting again.
- **Ambient Glow costs far less:** each new light is drawn once and faded by the system, instead of redrawing the window on every frame of a fade. On a test Mac, the app's main work with the glow on fell from 8.6 to 1.1 seconds in every 30.
- **The guide redraws less:** one channel's guide arriving no longer redraws every row on screen, each row's programmes are drawn in one go, and rows wait until scrolling settles before loading a full day.
- **Smoother sidebars:** moving the pointer down the Live TV and Guide sidebars no longer makes every row redraw, and scrolling holds about 120 frames a second.
- **All Channels without a hang:** long channel lists are sorted into rows in the background, with a spinner meanwhile, instead of freezing the window.
- **Channel logos** are kept ready in memory as you scroll. Clear Image Cache empties them.

### Fixes

- **Float Video** no longer crashes when you open it, or when you minimise the window while a video plays. The picture goes straight to the floating window, without passing through the mini-player, and Expand, double-click and Full Screen from the floating window now glide from where it is.
- **Full screen with Match Frame Rate** no longer goes black for a moment: the display's refresh rate changes once the picture has settled. Displays with a variable refresh rate, such as a MacBook Pro's built-in display, are left at their own rate.
- **Ambient Glow in the banners** now starts when the app resumes your last channel at launch and you open Live TV or the TV Guide.
- **The mini-player stays** when you choose a section in the sidebar while Now Playing is open.
- **Toolbar tooltips:** Now Playing, Multi-View, Refresh and Auto-Record each show their own tooltip, and VoiceOver reads Multi-View by its own name.
- **Home's banner** no longer changes slide while its window is in the background.
- **Fewer layout warnings** in the console when the picture moves between pages.

## v0.24.01: Smooth Picture Moves by default, HDR, stream colours, subtitles on hardware

Smooth Picture Moves is now on for everyone, with HDR, each stream's own colours, and subtitles that no longer cost the earth.

### Smooth Picture Moves, now the default

- **On by default:** the picture glides between the mini-player, Now Playing, the banners and title pages without a pause. If you turned it off, it stays off. The Beta badge is gone, and its description in Settings › Playback › Video now says what it does and what turning it off changes.
- **HDR:** HDR10 and HLG streams play in 10-bit and show in HDR, brighter than white, on displays that support it, with smooth gradients. Before, they were shown flat and washed out.
- **Each stream's own colours:** ElBee Player now reads the colour settings a stream carries (from its playlist, its file or the video itself) instead of guessing from the picture's size, so an HD stream made with SD colours, or the other way round, looks right from the first frame. Live channels sent as raw MPEG-TS aren't read, to avoid a second connection to your provider, and keep the usual choice.
- **Subtitles stay on hardware decoding:** turning subtitles on no longer moves decoding to the processor. On a test Mac, a 1080p channel with subtitles went from 33% of the processor to 7%, and a 4K 10-bit film from more than a whole core to 15%. They appear at once, with no pause, and 4K and 10-bit films now show subtitles too. HDR shows in 8-bit while subtitles are on, as they can't be drawn into 10-bit pictures.

### Live TV

- **Falls back faster:** when a provider refuses a channel's first address, ElBee Player moves on to the next at once (or within about 8 seconds if the provider answers with an error page), instead of retrying the first one for half a minute or more.
- **Remembers what works:** once a channel has played from its second address, it goes straight there for the rest of the session, reconnects included.

### Fixes

- **The standard player's colours:** with Smooth Picture Moves off, reds, magentas and blues were about 10% too strong on wide-colour displays. They now match.
- **Match Frame Rate** switches the display's refresh rate again in full screen, for live channels and films (it had stopped in v0.23.02).

## v0.23.02: Subtitle timing, a clearer Subtitles button, less work while playing

Subtitles you can line up with the dialogue, a clearer Subtitles button, and less work while you watch.

### Subtitles

- **Subtitle timing:** when a channel's subtitles run ahead of the dialogue or behind it, move them with **Show Earlier** and **Show Later** in the player's Subtitles button, or **View › Subtitles Earlier (⌘[)** and **Subtitles Later (⌘])**, in half-second steps. The timing is remembered for each channel, film and episode, and **Reset Timing** puts it back.
- **A clearer Subtitles button:** it's split into **Subtitles from the Channel** (Show Subtitles, Language and Timing) and **Live Captions · Made on This Mac**, so it's clear where each comes from. Language and Timing are now submenus, so the menu stays short however many languages a channel has.
- **One at a time:** turning on subtitles turns Live Captions off, and the other way round, so two lines of text never sit over the picture. Subtitles on by default no longer switch on over captions you've turned on.
- **One Text Size:** a single Text Size sets the size of whichever is showing. Subtitles a channel sends as pictures (most live TV subtitles) keep the channel's own size, and the menu says so rather than offering a size that can't change them.
- **4K subtitles with Smooth Picture Moves:** a 4K or 10-bit film stays on hardware decoding with subtitles on, rather than taking several processor cores. Its subtitles can't show with Smooth Picture Moves, and the Subtitles button says to turn it off for them.

### Lighter on your Mac

- **Less work while playing:** the player no longer refreshes its controls, the glow, the Now Playing info and the frame-rate check several times a second for nothing. They update when something actually changes, such as the picture's size or frame rate becoming known.

## v0.23.01: Casting, a playlist chooser at launch, and far lower energy use

Cast to a TV or speaker, a choice of playlist at launch, and a player that's far lighter on your Mac's battery.

### Casting

- **Cast to a TV or speaker:** a new Cast button sits with the other player buttons in the mini-player, the floating window, the banners, Now Playing, full screen and Radio. It lists the TVs and speakers on your network as they're found. Pick one and what's playing carries on there, from the same spot.
- **While casting**, the picture shows "Casting to" and the device's name, with **Stop Casting**. Play/Pause, the skips and the progress bar control the device. Its volume is set with its own remote, so Mute and the volume slider are greyed out, and Live Captions are off.
- **Stop Casting** brings playback back to your Mac from the same spot. If the device is switched off or leaves the network, playback comes back on its own, with a note saying so. Closing the video ends casting too.
- **Cast Quality** (Settings › Playback › Streaming & Data): how hard your Mac works when a device can't play a stream's format as it is, from Fastest to Best Picture.
- **Stays awake:** your Mac doesn't go to sleep while casting, as it's sending the stream to the device. Its display can still sleep.
- **The first time** you open the Cast button, macOS asks to let ElBee Player find devices on your local network.
- **For a TV that works with Screen Mirroring**, turn on Screen Mirroring in Control Centre and play in full screen on that display.

### Playlists

- **Choose a playlist at launch:** with playlists saved, ElBee Player opens on a chooser listing each one with its server's status, checked with its saved login. Click one, or press ⌘1 to ⌘9, to sign in. **Add Playlist…** opens the sign-in form, which now starts empty and has a **Back to Playlists** button.
- **Sign In Automatically To** (Settings › General › Startup): pick a playlist to sign in to as the app opens, without the chooser. **Ask Each Time** is the default. If the playlist can't sign in, the chooser opens with the reason. Hold Option as the app opens to see the chooser anyway.
- **File › Choose Playlist… (⇧⌘P)** goes back to the chooser.

### Lighter on your Mac

- **Far less energy while you watch:** ElBee Player no longer shows as using significant energy. On a test Mac, a 1080p film went from about 72% of the processor to 25–35%, and 4K plays at about 35–40%.
- **Ambient Glow is much cheaper to draw:** it's drawn at a fraction of its size and scaled up, and it only redraws when its colours change visibly, at most 30 times a second. It looks the same.
- **Smooth Picture Moves uses hardware decoding:** a wrong setting had made it decode every stream on the processor. Frames now go to the graphics chip in their own format, rather than being converted on the processor, and 4K pictures are no longer shrunk on the processor first.
- **Ambient Glow and the picture ready for the next glide** read the picture without holding the app up.
- **Deinterlacing skips pictures that are never interlaced:** 4K is never deinterlaced, and Auto leaves movies and episodes alone, since they're made progressive. Always still treats movies and episodes up to 1080 lines.

### Smooth Picture Moves (beta)

- **Subtitles:** they can only be drawn into a picture decoded on the processor, so turning subtitles on switches that stream to the processor for as long as they show, with a moment's pause, and turning them off switches back. While you're recording, the switch waits until the recording stops.
- **Colours match the standard player:** no more crushed shadows or harsh skin tones.
- **Widescreen films fill the glow:** with Ambient Glow on, the black bars above and below are trimmed off and the glow starts at the picture's own edge, lighting where the bars were. Not while subtitles show, as they may sit in a bar.

### Ambient Glow

- **Stays on for widescreen films:** it used to switch off when the picture had black bars. Now it takes its colours from the picture inside them.
- **Dark scenes** are no longer mistaken for black bars.

### Polish

- **The player's controls stay up** while the Cast list is open, so moving to a device no longer closes it.
- **Deinterlacing's description** in Settings says what Auto and Always now do.

## v0.22.01: Searchable Settings, new settings and shared player controls

Settings you can search, a tidier layout, clearer descriptions, a handful of new settings, and one set of controls for every small player.

### Player

- **One set of controls for every small player:** the mini-player, the floating window, the pictures in the Live TV and Guide banners, a title's page and Radio's banner all share the same glass controls: Play/Pause, the skips, the progress bar, Mute and volume, Expand to Now Playing and Full Screen last. With less room the volume slider goes first, then the progress bar, never a button.
- **A movie or episode plays on its own page:** while Now Playing is closed, the title's page shows the picture above its details, with the same controls and close cross. On other pages it plays in the mini-player. While a title plays, its page leaves out Play, Resume and Start Over, which would restart it.
- **The movie and episode banner is gone:** the banner that held a playing movie or episode across the top of every page (added in v0.20.01) has been removed. The Live TV and Guide spotlights and Home's new releases banner now stay put while a movie or episode plays; the spotlight shows the channel without a live preview then, since most providers allow only one stream.
- **Live Caption Size:** Live Captions have a size of their own, set apart from Subtitle Size, in Settings and in the player's Subtitles button while captions are on.

### Finding your way round Settings

- **Search Settings:** a search field at the top of every sidebar (⌘F) finds any setting by its name or by the words you'd use for it, such as "hotspot", "sleep" or "parental". Click a result, or press Return for the best one, and Settings opens on its page with the setting highlighted.
- **A tidier layout:** seven categories instead of eight. Multi-View is now a group in Playback. Subtitles & Captions and Audio are separate groups. Sport has its own group in Live TV & Guide, holding Ultra-Low Latency, Hide Sports Spoilers and Custom Sports Keywords. Series Link's auto-delete and free-space limit sit with the rest of Series Link. Use Full-Screen Spaces is in Playback › Player, Default Channel Category is in Live TV & Guide › Live TV, and Interface Size is in Appearance › Window & Text.
- **Every description rewritten:** shorter, and each says when the setting takes effect and what it leaves alone.
- **Clearer names:** Data Saver (was Travel & Tethering Mode), Hide Country Prefixes and Hide Provider Tags in Titles (were Strip…), Hide Sports Spoilers, Sharpening (was Video Upscaling: it sharpens rather than upscales), Night Mode, Even Out Volume (was Audio Normalisation), Match Frame Rate, Audio Language and Subtitle Language. Your choices are kept.
- **Restore Defaults on every page** puts only that page's settings back, leaving the rest as they are.
- **Greyed-out settings say why,** such as "Turn on Channel Spotlight to use this."
- **Beta badges** mark Live Captions and Smooth Picture Moves, and one banner with **Relaunch Now** appears when a setting needs the app to reopen.

### New settings

- **Play Next Episode Automatically** (Playback › Player, on): turn it off and Up Next waits for you to click Play Now, with no countdown.
- **Pause When Screen Locks** (Playback › Player): pauses when your display sleeps, your Mac locks or another user switches in. Radio carries on.
- **Remember Volume** (Playback › Audio, on): the player opens at the volume you left it at, instead of 100%.
- **Last Viewed** for Default Channel Category: Live TV and the TV Guide reopen on the category you were last in.
- **Switch to the Channel** (Live TV & Guide › Reminders): as a reminder appears, its channel starts too, while ElBee Player is open.
- **Re-Lock After** (Content › Parental Lock): unlocked categories lock again after 5 minutes, 15 minutes or an hour, or as before when the app quits. A longer time asks for Touch ID or your password.
- **Hide Locked Categories** (Content › Parental Lock): leaves locked categories out of the sidebar, the lists, the TV Guide and search. Showing them again asks for Touch ID or your password.
- **Image Cache Limit** (Storage › Cache, 1 GB): how much space logos and posters may take before the oldest make room.

### Polish

- **Clicking a reminder** now opens its channel.
- **TV Guide:** programmes no longer sit on top of one another when a provider sends the same programme twice or listings that overlap; each channel shows one programme at a time, and "on now" is always the right one. Guide data already saved is tidied too.
- **The mini-player's glow is gone:** the Ambient Glow that spread from the mini-player across the page beside it (added in v0.21.01) has been removed. Ambient Glow still lights full screen, Now Playing and the banners.
- **TV Guide:** the calmer programme grid and the row of day buttons are now the only look, so Quieter Programme Cells and Day Buttons are gone from Settings.
- **Live TV & Guide** opens on its Live TV page again after Settings is reopened, not on Guide Data.
- **Reset Library** names the iCloud setting correctly.

## v0.21.02: Roll-up Live Captions

Live Captions that are easier to follow.

### Player

- **Live Captions roll up, two lines at a time:** words appear one after another at the end of the bottom line, and when it's full the line moves up and a new one starts below. Words you've already read stay where they are instead of shuffling along with every new word, and the plate keeps one size. Words the Mac is still working out are a little dimmer and settle once it's sure of them. Speech carries straight on from one phrase to the next, and the captions clear after a few seconds of quiet.

## v0.21.01: In-place full screen, Live Captions and banner glow

Full screen in one smooth move, Live Captions, and the picture's glow behind the banners.

### Player

- **Full screen in one smooth move:** the picture grows from where it is to fill the screen, and shrinks back to Now Playing, with no slide to a new Space. The menu bar and Dock hide while you watch and come back when you point at them. If you'd rather have full screen in a Space of its own, to swipe between it and your other apps, turn on Settings › Playback › Display › Use Full-Screen Spaces.
- **Live Captions (experimental, macOS 26):** your Mac can write captions for live channels that have no subtitles of their own, from the channel's sound, on your Mac. Turn them on in Settings › Playback › Subtitles & Audio (after a restart), then from the Subtitles button.

### Polish

- **Ambient Glow behind the banners:** the Live TV, Guide and movie banners take on the picture's light, and the mini player's glow spills out across the page beside it.
- **One click** on a banner's picture opens Now Playing.

## v0.20.01: Movie banner, live Subtitle Size, quiet launch resume

A banner for movies and episodes, a live Subtitle Size, a quieter launch and a round of polish.

### Player

- **A banner for movies and episodes:** pressing Back from Now Playing while a movie or episode plays now flies the picture into a banner at the top of the page, as Live TV does, instead of the mini player. It shows the title (and episode), how far through you are, and the usual controls over the picture. It appears on every page except Live TV, the TV Guide and Radio, which keep their own banners.

### Polish

- **Opening the app** no longer flashes a "Signing in…" screen before the loading screen: the logo shows alone, in the same place as on the loading screen, and the status only appears if signing in takes more than a moment.
- **TV Guide:** every programme block, including the one on now, and every channel in the list brightens under the pointer, in either cell style.
- **Live TV:** channels near the bottom of the list highlight under the pointer again while something is playing; the room left for the mini player no longer blocks them.
- **Reconnecting…** now shows over the picture in the Live TV and Guide banners, and in the movie and episode banner, as it does in the other players.
- **A movie or episode keeps the top banner** when you go to Live TV or the TV Guide, instead of dropping into the mini player. Their channel banners step aside meanwhile, and a click on a channel plays it. Home's new releases banner steps aside too, so there is never a second banner under the first.
- **Resume Last Channel on Launch:** if the channel can’t be reached, or its picture stays black for ten seconds (a provider keeping a channel that is down on air as a black feed), it is dropped quietly and you stay on the page you opened on, with no player left over. The mini player or banner picture doesn't show until the first real frame arrives, so a dead channel never flashes a black box.
- **Subtitle Size:** Settings › Playback › Subtitles & Audio sets how large subtitles are drawn (Small, Standard, Large or Extra Large), from the next stream you start. The Subtitles button on Now Playing and in full screen has the same choice. The text changes at once, without restarting the stream.
- **Ambient Glow** switches itself off while the picture has thick black bars of its own, and comes back when they go.
- **Toolbar:** the section tabs and the buttons beside them light up softly under the pointer.

## v0.19.01: Plain Look and Smooth Picture Moves

A plainer look if you want one, and Smooth Picture Moves: an experimental way of drawing the video that removes the pause when the picture moves between pages.

### Moving the picture

- **Smooth Picture Moves (experimental):** Settings › Playback › Display. ElBee Player draws each video frame itself, so the picture can move between the banner, the mini player and Now Playing without the short freeze. It applies after you quit and reopen the app, and is off by default.
- **Hardware decoding stays on,** and subtitles are drawn on the picture as usual, including on 4K.
- **No thin black bars** at the sides of the picture, and the picture keeps its own shape.
- **Deinterlacing with Yadif 2x** works with it.
- **One refreshed still** is used as the picture lands, so the glide no longer stutters on arrival.

### Appearance

- **Plain Look:** Settings › Appearance › Window swaps the system glass for a plainer surface everywhere in the app.

### Fixes

- **Back from the live dashboard** returns to the page you came from, and the picture glides back with you.
- **The mini player's control bar** is a single tidy capsule, with the sliders sized to fit.
- **Dark mode:** the Now Playing stage no longer fades slowly when you go to Live TV or the TV Guide.
- **Fanart:** the blurred backdrop on title pages loads once, without a flicker or seam, and the Guide banner backdrop suits both light and dark.

### Known issues

- Back from a movie or episode goes to the mini player rather than the Guide. (Fixed in the next release.)

## v0.18.01: Uniform player controls, glass close cross, hover controls on the live preview, and a rebuilt picture glide

Players that look and behave the same everywhere, a smoother glide to and from the banner, hover controls on the live preview, and a round of fixes to Live TV, the TV Guide and Settings.

### Player

- **One set of controls everywhere:** the mini player, Now Playing and full screen use the same buttons, icons and order, with Full Screen always last. Full screen's button changes icon, and leaving full screen always returns to Now Playing.
- **A glass close cross replaces Stop:** every player shows a cross in its corner that closes the video completely. It appears when you move the pointer over the picture and fades away with the controls.
- **A cleaner mini player:** the grey control area is gone. Pause, the progress bar, volume and the buttons to open Now Playing and full screen sit over the picture when you point at it.
- **Expand to Now Playing** has its own button, next to Full Screen.
- **All player controls sit on the same glass,** including badges, banners and the skip pill.

### Live TV and TV Guide

- **The live preview has controls:** click Muted to turn the sound on, then point at the picture for Mute, Expand to Now Playing and Full Screen. Double-click the picture to open Now Playing.
- **The picture stays in the banner while you browse categories,** instead of dropping to the mini player when the new category doesn't hold the channel.
- **Right-click a combined channel** to choose which version to play. The sharpest picture (for example 4K) is marked Best Quality, while the row still plays HD by default.
- **Switching Combine Duplicate Categories** keeps you where you are and no longer closes Now Playing.
- **Strip Country Prefixes and Group Categories by Country now work together:** names follow the strip setting everywhere, and the headings carry the country.
- **A new preview takes the sound of the last one:** if you were listening, it starts with sound.
- **Channel changes are quicker:** the banner waits 250 ms before tuning, covers the picture with a blurred frame until the first frame is on screen, then crossfades in 0.15 s.
- **The TV Guide opens faster:** its rows are worked out in the background and kept.

### Moving the picture

- **The picture glides** between the Live TV and Guide banners, the mini player and Now Playing in either direction, flying out at the click and landing as the page appears. It keeps playing while it moves.
- **Stable between pages:** swapping between Live TV and the Guide no longer risks a black picture.

### Loading screen

- **Every step starts grey** and lights up only when it has finished loading, with the same spinner on each.

### Settings

- **Appearance › Home Screen:** New Releases can be switched off, but always stays at the top.
- **Storage › Cache** shows the real sizes again and Clear is available.
- **About** fits the window without scrolling.
- **Ambient Glow is on by default** for new installs.

### Known issues

- Going from Now Playing to the TV Guide still takes a moment to change page.
- The picture is a little softer than the live video for a moment as it lands.

## v0.17.01: Live TV, TV Guide and Radio redesigns, live preview, and first-time setup

Redesigned Live TV, TV Guide and Radio pages in Home's style, with a live preview, a first-time setup guide, and a calmer, steadier player.

### Live TV

- **Channel spotlight:** click a channel to see it in a banner at the top: what's on, how far through it is, what's next, and Watch, Record and Favourite. Double-click to play straight away.
- **Live preview:** the clicked channel plays, muted, in the banner instead of the mini player. It uses your one stream, never a second one. It waits a moment as you click down the list, and holds back while you're recording, watching a movie or episode, or using Multi-View.
- **One row per channel:** HD, 4K, +1 and other versions share a row, as buttons that play each one.
- **Now and next in each row,** with sort, find, ↑ / ↓ to move the spotlight, and Return to play.
- **Sidebar headings for each country** (and for other prefixes), which fold away.

### TV Guide

- **Programme spotlight:** click a programme for its details. You can watch it if it's on now (with the live preview), set a reminder or Series Link if it's later, or watch from catch-up if it has finished.
- **Day buttons** with **Now**, and All / Favourites / Catch-Up.
- **Quieter grid:** bells only where a reminder is set, a thin progress bar for what's on, earlier programmes dimmed, and an amber now line with the time.

### Radio

- **Station tiles** coloured by genre, **genre buttons**, a **Recently Played** shelf, and the station playing in a **Now Playing banner** with its controls. Tiles play without leaving the page.

### Getting started

- **First-time setup:** after signing in to a new playlist, a short guide covers languages, categories, the guide, what to open on, text size, Ambient Glow and the parental lock.
- **A new sign-in screen** that flows into the loading screen. The loading screen now also fetches the TV Guide for up to 200 channels.
- **Erase Everything** reopens the app on the sign-in screen.

### Player

- **Subtitles button on Now Playing,** with Show Subtitles and a language list. Subtitles no longer flicker, and the controls sit below the picture while they're on.
- **Mute stays on** for what you play next, until you unmute or quit.
- **← / → skip** without bringing up the controls.
- **Smoother Ambient Glow:** it follows scene changes at once and smooths out flicker. Full screen's glow is softer.
- **A tidier glide** between Now Playing and the mini player, with no black bars or lingering box.
- **The heart is in the same place on every player.** On movie and series pages, it's a heart button beside Trailer.

### Settings

- **New and moved settings:** Appearance › Channel Lists, Content › Names & Grouping, and a new **Live TV & Guide** tab, so each setting sits where you'd look for it. Every redesign can be switched back.

## v0.16.01: Advanced Video, ambient light, Now Playing for movies and episodes, and system glass

Advanced Video in the player, ambient light round the picture, movies and episodes on Now Playing, Up Next as the credits roll, and the system's own glass across the app.

### Advanced Video

- **A new Advanced Video menu** in the player (the sparkles-TV icon), also in Settings › Playback › Video.
- **Ambient Glow:** soft light round the picture in the colours at its edges, three zones to a side, following the picture five times a second. It fills the bars in full screen, spreads under the sidebar and into the page on Now Playing, glows in Dark Mode and tints (or, for dark scenes, softly shades) the page in Light Mode.
- **Match Framerate:** in full screen, the display switches to a rate that fits the stream (50 Hz for 25 or 50 fps, 59.94 Hz for 29.97, and so on) and switches back afterwards.
- **Deinterlacing** now offers Auto and **Yadif 2x** (50 full frames a second from 50i sport), and changes apply to the stream already playing.

### Now Playing

- **Movies and episodes** now open on the Now Playing page too, with their details, cast, episode plot and the episodes up next, plus a seek bar.
- **Up Next appears as the credits begin**, detected from the picture, with a 6-second countdown, Play Now and Keep Watching; otherwise in the final minute.
- **← / → seek, Space pauses**, and the "+10s" pill shows, as in full screen.
- **The picture glides** between Now Playing and the mini player.
- Leaving full screen returns to Now Playing; Back no longer restarts an episode.

### Look and feel

- **The system's own glass** for the toolbar, player controls, mini player, pop-ups and their buttons on macOS 26.
- **The mini player** now sits in the sidebar above the playlist bar.
- **Home's banner** runs edge to edge, up under the toolbar and under the sidebar.
- **Light, Dark or Automatic** for ElBee alone, in Settings › Appearance › Window or from the sun and moon button by the Settings gear, crossfading like the system switch.
- **A livelier loading screen**: a drifting amber glow, a progress bar and a checklist of what's loading, finishing cleanly even when the library opens from its cache.
- Softer poster hover, Window Background Opacity (Dark Mode) replaces the old vibrancy setting, and Light Mode's sidebar and toolbar now match the system.

### Fixes

- No white bar at the top of the screen in full screen, and no header flashing as it opens.
- The Reconnecting pill clears as soon as the picture is back.
- Ambient Glow and Match Framerate keep working when a stream restarts.

## v0.15.01: Home screen, Content Languages and reorganised Settings

A new Home screen, content in the languages you choose, and a reorganised Settings window.

### Home

- **Home is the first tab and the screen the app opens on.** It replaces the Library tab; Favourites and History are in its sidebar.
- **New releases banner** with backdrops, plots and Play or More Info.
- **Continue Watching**, and your favourite channels as **On Now** tiles showing what's on, how far through it is and what's next.
- **Recommended for You**, chosen on your Mac from what you watch, favourite and finish: genres, categories, franchises and more, with the reason under each poster. Plus **Because You Watched** your latest title.
- Favourite movies and series on short shelves at the bottom.
- **Arrange Home** in Settings › Appearance › Home Screen: reorder sections or switch any off.
- Titles show without provider tags such as “TOP - ” or “4K - ”.
- Choose a different start screen in Settings › General › Startup › Open On.

### Content

- **Content Languages** replaces Hide Non-English: tick the languages you want, and only categories, channels and titles in those languages show, everywhere in the app. It recognises tags such as NL|, FR -, NL-TOP - and 4K-NL -, words and scripts.
- **Strip Provider Tags from Titles** cleans movie and series titles on every page.
- **Right-click a category** in the sidebar to reorder its channels, hide it, or lock it.
- The catalogue now refreshes quietly every 3 hours, so new releases appear without restarting (not while saving data).

### Settings

- **Reorganised:** the icons along the top are categories, each with a sidebar of groups, and a new Content category.
- **Every setting now explains exactly what it does.**
- **Manage Categories** is now inside Settings › Content › Categories (⌘⇧K still opens it), with the selection's actions in one menu.
- **Interface Size, Open On and more reset options** are covered by Reset Settings; Settings opens centred.
- The sidebar footer is one line: playlist and Settings.

### Fixes

- Clicking the current tab returns to its main page, for example Home from a movie page.

## v0.14.01: Section tabs, faster TV Guide, Interface Size and reset options

A new window layout with section tabs across the top, a faster TV Guide you can drag around, and new settings for text size, your starting category and resetting the app.

### Layout

- **Section tabs in the toolbar.** Live TV, TV Guide, Radio, Movies, Series, Recently Added and Library sit in one bar across the top, centred on the window. In a narrow window they switch to icons.
- **Two columns.** The sidebar now shows the chosen section's categories, so there is more room for what you're watching.
- **Library tab.** Favourites and History live together under Library, with a filter for what to show.
- **Now Playing button.** Jumps to the channel that's playing, or says so when nothing is.
- **Radio Stations and Guide** are chosen at the top of the sidebar.
- **One glass toolbar.** The buttons, tabs and a new search field share the same frosted glass, with a soft glass fade under the toolbar in Dark Mode. The window drags only from the empty space around them.
- **Hover highlights and tooltips** on sidebar rows, like the channel list.

### TV Guide

- **Channel names stay in view** as you scroll through time, and the "now" line no longer runs over them.
- **Faster scrolling,** especially with a full guide.
- **Drag to move around** the guide with a mouse.
- **Day controls** sit under the section tabs.
- No programme tooltips over the full-screen player.

### Settings

- **Interface Size** (Appearance): Automatic, Large, Extra Large or Maximum makes text larger throughout the app, for example on a high-resolution display.
- **Default Channel Category** (General): Live TV and the TV Guide open on the category you choose. Set per playlist.
- **More reset options** (General): reset settings, your library, your category choices, or erase everything and start again.

### Fixes and polish

- **New app icon,** the Antenna TV set.
- Movies open without a pause.
- Light Mode: no dark strip at the top, and readable text over backdrops. Dark Mode: no flicker in the header.
- Toolbar icons are all the same size.

## v0.13.01: Richer detail pages, Light Canvas icon and migration clean-up

A richer Movies and Series page, a new app icon, and a tidier update path.

### Movies and Series

- **You May Also Like.** A shelf of posters under the details, from the same category, with titles that share a genre
  first. Click one to open it.
- **Fanart backdrop.** When your provider supplies one, a faded image sits behind the page.
- **Watch Trailer.** A button that opens the trailer in your browser, when the provider lists one.
- **Cast and director as chips.** Names wrap neatly onto as many lines as they need instead of one long string.
- **Season picker.** Series show one season at a time, chosen from a dropdown. It opens on the season you are watching.
- **Tidier episode rows.** Provider prefixes are removed from episode names, with the air date and run time beneath. Stills
  and descriptions appear when the provider supplies them.
- **Age ratings.** A badge appears beside the star rating when the provider sends one (many do not).

### Appearance

- **New app icon,** a light glass tile with an amber hexagon, also used on the launch, sign-in and About screens and in
  the sidebar's playlist selector.
- **Refresh menu.** The refresh button is now a menu: Refresh All, Refresh Category, Refresh Movies and Refresh Series.
- **Calmer colours.** Hearts are red, Event tags match the other tags, and the app's accent is amber throughout,
  including the Settings tabs.

### Updating

- Updates no longer carry a second copy of the app for the old name. Settings and playlists from before ElBee Player's
  rename are no longer imported, since that carry-over has long since run.

## v0.12.01: Amber theme and Prism app icon

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

## v0.11.02: Updating fixes for copies installed under the previous name

Fixes updating to ElBee Player from inside the app. There are no other changes.

### Updating

- **Copies installed under the old name can now update.** The in-app updater could not install version 0.11.01 on a copy
  still called LiquidIPTV, and reported the update as improperly signed. That message was misleading: the updater picks the
  app to install by the installed app's file name, and the rename had changed it. Updates for those copies now carry the app
  under the name they expect. Your data comes across as described for 0.11.01.
- **The app may keep its old file name** in your Applications folder after updating (it still says ElBee Player inside).
  You can rename it to ElBee Player in Finder at any time. Later updates work either way.
- Version 0.11.01 can still be downloaded and installed by hand; it simply could not be installed by the updater.

## v0.11.01: A new name: ElBee Player

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
  - **Appearance:** keep the window on top, glass strength with *Reset to Default*, show channel logos in lists, and
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
