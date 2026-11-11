# Changelog

All notable changes to ElBee Player are listed here, newest first. Earlier releases are described on the
[GitHub releases page](https://github.com/ElBeeHQ/ElBeePlayer/releases).

## v0.40.05: Polish (11 November 2026)

The full-screen player's controls take less of the picture, the small players are tidier, and switching playlist now stops what was playing.

Your settings are all kept: none was renamed or reset.

### In short

- The full-screen and Now Playing controls fit on fewer rows, so they cover less of the picture
- The floating video window works like Picture in Picture
- Switching playlist stops the video straight away

### Changed

- **Full-screen controls:** Subtitles, Cast, the volume, More and Full Screen stay on the same row as the playback buttons whenever they fit. In a narrower window the volume slider folds into the speaker button (click it to change the volume) before anything moves to another row. The bar's top and bottom padding is smaller.
- **Small players:** the playback buttons stay on one row; "Expand to Now Playing" no longer drops onto a line of its own.
- **Floating video:** smaller controls and a smaller close button; Restart, back, Play/Pause, forward and LIVE in the middle; Open Player in the corner opposite the close button; a Mute button; a thin progress line along the bottom edge (a seek bar for catch-up, films and episodes) and the programme's title when you point at the picture. Drop it near a screen corner and it settles into the corner. It keeps its size and place, and shows over full-screen apps and in every Space.

### Fixed

- **Switching playlist:** the video that was playing stopped only when switching from Settings. It now stops the moment any switch starts, and the Now Playing bar clears, before the new playlist signs in.

## v0.40.04: Keychain (11 November 2026)

All your playlists' sign-ins are now kept together in one keychain item, so after an update macOS asks for your keychain password once, not once for every playlist you've saved.

**After this update macOS may ask for your keychain password one more time for each playlist you've saved.** Enter your password and click **Always Allow**. From then on, an update asks at most once.

Your settings and playlists are all kept: none was renamed or reset.

### In short

- After an update, macOS asks for your keychain password once at most, instead of once for each playlist
- Your playlists' sign-ins are in one keychain item, called "ElBee Player sign-ins"

### Changed

- **One keychain item:** your playlists' names, addresses, usernames and passwords are kept together in one keychain item instead of one for each playlist. They're moved there the first time this version opens, and the old items are removed only once the new one has been checked. If anything goes wrong, the old items are left as they were and it tries again the next time you open ElBee Player.
- **Why macOS may ask after an update:** macOS checks once that you still allow each new version of ElBee Player to use your keychain. Enter your password and click Always Allow.

## v0.40.03: Performance (10 November 2026)

Live TV uses far less energy with a channel playing, hiding or showing the sidebar is smoother on the TV Guide and Live TV, and the welcome's buttons are the standard macOS buttons.

Your settings are all kept: none was renamed or reset.

### In short

- Live TV with a channel playing uses about a quarter of the processor it did
- Hiding or showing the sidebar on the TV Guide drops about half as many frames as before
- The welcome, the inspector and other sheets use the standard macOS buttons

### Fixed

- **Live TV energy:** the moving waveform beside the playing channel made the whole channel list redraw at the display's full rate for as long as the channel played. It's now drawn by macOS itself, as Home's already was, and an idle Live TV page with a channel playing uses about a quarter of the processor it did.
- **TV Guide sidebar:** hiding or showing the sidebar laid out and redrew every programme on screen about ten times. Each row now redraws only when its own programmes change, the bar above the grid works out its layout from its pieces' own widths instead of trying every arrangement, and the programme titles stay where they are until the sidebar has finished moving.
- **Fewer redraws when the window saves its layout:** the TV Guide's Show choice and View ▸ Hide Toolbar and Hide Now Playing Bar no longer make their pages redraw whenever any other setting is saved.

### Changed

- **Buttons:** the welcome, the empty window's Add Playlist…, the loading screen's Continue, Not Interested's Done, Choose File… and the buttons in the Live TV and TV Guide inspector are the standard macOS buttons, with the default button in the accent colour, as in Apple's own apps. Buttons over a picture (Home's banner, a title's page, Skip Intro and Up Next) keep their glass.

## v0.40.02: Layout (10 November 2026)

The Now Playing bar, the toolbar's search field and the categories column fit the window at every width and every Interface Size.

Your settings are all kept: none was renamed or reset. A categories column width you dragged is kept too.

### In short

- Nothing in the Now Playing bar overlaps any more, however narrow the window
- The search field stays in its own column, beside the inspector or above it, and shrinks to a magnifier where it doesn't fit
- The categories column opens wider, and wider still at the larger Interface Sizes, so names like "UK | Documentaries Spotlight HD" aren't cut short

### Fixed

- **Now Playing bar:** beside the inspector in a window about 1,050 points wide, the picture covered the Next button. The bar now keeps every item clear of the others at any width: the volume slider goes first, then the summary's second line, and in the narrowest places the summary moves onto a row of its own above the buttons. No button is ever dropped, and pages keep their last row clear of the taller bar.
- **Search field and the inspector:** the inspector on Live TV and the TV Guide is now a column of the window itself, as in Apple's own apps, with its own part of the toolbar. While it shows, the inspector's button and the search field sit above it, inside it, and the search field shrinks to a magnifier when there isn't room; it no longer runs across the inspector's edge. The toolbar's buttons and their order are unchanged.

### Changed

- **Inspector in a narrow window:** the inspector no longer hides itself when the window gets narrow. While it's open the window can't be made narrower than the sidebar, the categories, the page and the inspector need side by side (about 1,060 points with the sidebar shown); close it with its button for a narrower window. Opening it in a narrow window widens the window to fit.
- **Categories column:** it opened at 200 points whatever the window or the Interface Size, so longer names were cut short. It now opens at least 230 points wide (more in a roomier window, up to 300), and its width follows Settings › Appearance › Interface Size as its text does: up to 40% wider at Maximum. A wider width you've dragged is still remembered.

## v0.40.01: Welcome, Not Interested and Automatic Rows (10 November 2026)

A first-run welcome that sets up your playlist in the main window, a way to tell Home you're not interested in a title, and rows Home builds for you.

Your settings are all kept: none was renamed or reset. If you had switched Because You Watched off, it stays off.

### In short

- A welcome the first time you open ElBee Player: add your playlist, watch it load, and start browsing as soon as Live TV and Movies are in
- Not Interested on Home's suggestions and banner, with Undo
- Hide Title is now Hide Everywhere…, and asks first
- Automatic Rows on Home: Because You Watched, 4K Films, Sport On Now, Newly Added Series, New Episodes and More of Your Genre
- New in Settings › Appearance: Automatic Rows and Suggestions

### New

- **Welcome:** the first time ElBee Player opens with no playlist, the main window walks through four short steps, each filling the window: Welcome, Add Your Playlist, Loading Your Library and You're All Set. Then Home opens and the sidebar slides in. Anyone who already has a playlist never sees it.
- **Add Your Playlist:** sign in to a server or add an M3U playlist by address or file (choose it or drop it on the window). Paste Link fills the form from a link on the clipboard, and only reads the clipboard when you press it. A wrong password, a server that doesn't answer and an expired account each say what happened in plain words, keep what you typed and put you where the fix is.
- **Loading Your Library:** a real progress bar and a checklist for Live TV, Movies, Series and the TV Guide, each with its count as it arrives. Start Watching opens the library as soon as Live TV and Movies are in; Series and the guide carry on in the background. Cancel stops the load and takes you back with your details kept.
- **You're All Set:** what arrived, and the two choices most people make first, Show Content In and Hide Country Prefixes, as the same settings you'll find later in Settings › Playlists.
- **Set Up Later:** leaves an empty window with one button, Add Playlist…, that picks up where you left off. File ▸ Add Playlist… (⌘N) adds a playlist at any time.
- **Not Interested:** right-click a title in Recommended for You, Recently Added Films or an automatic row, or use the banner's new More (…) button, and choose Not Interested. Home stops suggesting it, in every version it comes in. For 8 seconds an Undo takes its place, while the row around it holds still, and ⌘Z brings it back after that. The title stays in Movies, Series, search and your favourites.
- **Learn from Not Interested:** Home also suggests a little less of what you mark, fading over about two months. Turn it off in Settings › Appearance › Suggestions, where Not Interested Titles lists what you've marked, per playlist, with Restore and Restore All.
- **Automatic Rows:** Home builds up to six rows from your library and what you watch: Because You Watched, 4K Films, Sport On Now, Newly Added Series, New Episodes and More of Your Genre. A row shows only when there's enough for it, a title appears in one automatic row at most and never in a row and the banner at once, and hidden, locked and other-language titles are left out. Right-click a row's title to hide it or find it in Settings.
- **Settings › Appearance › Automatic Rows:** tick the rows you want and set their order; Home's own list places them as one block. New Episodes is off until you tick it, because it asks your provider about each series you watch (at most 20, once a day, never on Data Saver).

### Changed

- **Hide Everywhere…:** Hide Title has a clearer name and asks before it hides a title from every page. Hide Channel is unchanged.
- **Because You Watched:** is now one of the automatic rows. It shows up to 20 titles and appears once it has 6.
- **VoiceOver:** each welcome step's title is a heading and is read as the step appears, the loading rows read as one item each ("Movies, 12,406 films, done"), Not Interested is an action on Home's cards, a marked title is announced with "Undo available", and the automatic rows' titles are headings with Hide This Row and Show in Settings… as actions.

## v0.39.02: Visual Fixes (10 November 2026)

Home, the film and series grids, Live TV and the empty pages read more clearly.

Your settings are all kept: none was renamed or reset.

### In short

- A Home banner without a wide picture is filled with a soft, blurred copy of the title's poster
- Film and series titles can take two lines, and the quality badge sits on the year line
- Category names written in capitals read in normal capitalisation, and the categories column can be made wider
- The Live TV inspector's buttons always fit, with "Open Player" in full
- Channels without a guide say so quietly
- Every empty page looks the same, with one thing to do next

### Improved

- **Home banner:** a title that has only a poster now fills the banner with a softly blurred, enlarged copy of that poster, instead of a plain colour with the top half empty. The poster and the text stay where they were, and titles with a wide picture look exactly as before.
- **On Now:** a channel whose programme has ended with nothing listed after it shows the channel's name with "No guide for this channel" under it, instead of its name twice. VoiceOver reads the programme first, then the channel.
- **Poster grids:** a title can wrap onto a second line before it's shortened, and every card keeps the same height so rows stay level. The quality badge (4K, HD and so on) now sits on the year line.
- **Tidy titles everywhere:** Search and More Like This name titles the same way the grids, title pages and Now Playing do, following Hide Provider Tags in Titles.
- **Categories:** a category name written all in capitals, such as "UK | MOVIES HD", reads "UK | Movies HD", keeping codes like UK, HD and 4K. Names already in mixed case are shown as your provider wrote them. The categories column can be dragged wider in a larger window.
- **Live TV inspector:** when the buttons don't fit on one line at the inspector's narrowest, or at a larger Interface Size, they move onto a second line instead of being cut short. The TV Guide's inspector does the same.
- **Channels without a guide:** the inspector, Live TV's rows and the search page's channel rows show a quiet "No guide for this channel" line where the programme would be. While the guide is still on its way, the inspector says "Loading guide…" and the rows show nothing yet.
- **Empty pages:** Favourites, History, an empty category, In Progress, search with no results, Recently Added, Catch-Up, the TV Guide's filters, Downloads & Recordings and the rest now share one empty state: an icon, a short title and line, and a button for the obvious next step where there is one, such as Browse Live TV or Clear Search. Couldn't Load Episodes now has Try Again.

## v0.39.01: Pause and Rewind Live TV (Beta) (9 November 2026)

Live TV can now be paused, rewound and taken back to live, even on channels without a catch-up archive. It's a Beta, off until you turn it on in Settings › Playback.

Your settings are all kept: none was renamed or reset. With Pause and Rewind Live TV off, nothing changes.

### In short

- Pause a live channel and carry on from where you paused (Beta)
- Rewind and skip through what you've watched since you tuned in, and jump back to live
- Now Playing and the Now Playing bar show how far behind live you are
- Channels with a catch-up archive keep Start from Beginning and their own rewind
- Choose how far back you can rewind, from 30 minutes to 4 hours

### New

- **Pause and Rewind Live TV (Beta):** in Settings › Playback › Player. While it's on, ElBee Player keeps the channel you're watching on your Mac from the moment you tune in, through the same single connection to your provider.
  - **Pause:** from Now Playing, the Now Playing bar, Space, the Playback menu, the media keys or Control Centre. Play carries on from where you paused.
  - **Rewind:** the live line becomes a seek bar over everything kept. Rewind and Skip Forward, and ← and →, move by your Skip Interval. LIVE jumps back to live.
  - **Behind live:** Now Playing shows BEHIND LIVE and how far ("−4:12"), and so does the Now Playing bar.
  - **Catch-up channels:** a channel with a catch-up archive keeps Start from Beginning, Rewind 1 Minute and the archive's seek bar. Pausing it uses the copy, and rewinding from a pause counts back from the paused picture.
  - **Rewind Up To:** choose how far back you can rewind: 30 minutes, 1 hour (the default), 2 hours or 4 hours. Older minutes are deleted as the channel plays, and a change applies at once.
  - **Storage:** the copy takes about 6 GB an hour of a high-definition channel and 13 GB of 4K, and its oldest minutes also go while your Mac has under 10 GB free. It's deleted when you change channel, close the video or quit, and anything left after a crash is deleted the next time ElBee Player opens.
  - **Before it turns on:** the first time you turn it on, ElBee Player says what it stores and that recording continuously adds wear to your Mac's storage. Turn On goes ahead; Cancel leaves it off. You're asked once on each Mac.
  - **Plays live as before:** casting, Multi-View, Catch-Up, and providers that turn the copy away.

### Improved

- **Settings:** the Categories page's note and Appearance › Home's note are one line each, with the rest behind their ? button.
- **Settings:** the Downloads and Recordings folder settings each say where the other is.
- **Settings:** an unused stored setting has been removed.

## v0.38.05: Easier Settings (9 November 2026)

Settings is easier to find your way round: a new Parental Controls tab, settings where you'd look for them, and one short line under each, with the rest behind its ? button.

Your settings are all kept: none was reset, and settings that moved or were renamed keep their values.

### In short

- A new Parental Controls tab, with everything for locked categories
- Shorter descriptions, with more detail behind each ? button
- Several settings moved to where you'd look for them first
- The playlist list is easier to read, and Categories shows tidied names

### Improved

- **Parental Controls:** locking categories with Touch ID or your password, Re-Lock After, Hide Locked Categories and choosing which categories are locked now have their own tab, between Appearance and Advanced.
- **Moved:**
  - Sign In Automatically To is in General › Startup, under Open On.
  - Keep Window on Top is in Playback › Windows & Full Screen.
  - Multi-View's settings are in Live TV.
  - Programme Inspector sits with Channel Inspector in Live TV › Live TV.
  - Ultra-Low Latency for Sport is in Advanced › Streaming & Data.
  - Advanced › Video is now Video, and Decoding & Diagnostics.
  - Playlists has Languages, and Tidy Names and Categories with Manage Categories….
- **Renamed:**
  - Sync Favourites & Continue Watching via iCloud is now Sync with iCloud.
  - Lock Categories with Touch ID or Password is now Lock Categories.
  - Hide What’s Next in Narrow Windows is now Hide What’s Next When Narrow.
  - VOD Downloads Folder is now Downloads Folder.
- **Search:** Settings search finds every setting by its name, and by its old name or old place.
- **Playlists:** a selected playlist is shown in grey, as in the main window, so its orange or red status stays readable. Every playlist shows its type, its state and any expiry.
- **Categories:** names show as they do in Live TV, tidied by your playlist settings. Filtering still matches the provider's own name.

## v0.38.04: Live TV and Reliability (9 November 2026)

Live TV opens again without asking for programme guides it already has, and the Now Playing bar is easier to reach with VoiceOver.

Your settings are all kept: none was renamed or reset.

### In short

- Going back to Live TV reuses the guide it already fetched
- Live TV asks for fewer guides while you scroll or use VoiceOver
- A channel that needs its second stream address no longer looks like an unexpected stop in diagnostics
- The Now Playing bar's controls are all labelled for VoiceOver

### Improved

- **Guides reused:** a channel with no guide, or only programmes that have ended, is remembered for a while like any other guide, so opening Live TV again doesn't ask for it each time. Real failures are still retried.
- **Fewer guide requests:** a Live TV row now waits a moment before asking for its guide, so rows that only flash past (a quick scroll, or VoiceOver reading through the list) ask for nothing. A reused row now asks for its new channel's guide.
- **Clearer diagnostics:** when a channel's first stream address fails and the next one plays, the stream log now gives the reason for the stop instead of calling it unexplained.
- **Accessibility:** the Now Playing bar and each of its controls (Previous, Play/Pause, Next, the picture and title, Mute, Volume and Float Video) are checked to be reachable and labelled, as VoiceOver finds them.

## v0.38.03: Now Playing Bar (9 November 2026)

Now Playing Bar: clearer text over colourful content, matching glass edge, more visible progress, tidier spacing.

Your settings are all kept: none was renamed or reset.

### In short

- The bar's programme and title read clearly over colourful pictures
- The bar's glass has the same edge as the Now Playing controls
- The progress line is easier to see
- Tidier spacing on the bar's right side

### Improved

- **Clearer text:** a faint, soft backing sits behind the bar's title and programme only, so they no longer take on the colour of what's behind the bar. The rest of the bar stays clear glass.
- **Matching glass edge:** the bar has the same light rim as the Now Playing controls.
- **More visible progress:** the unfilled part of the progress line is a little stronger, and stronger again with Increase Contrast on.
- **Tidier spacing:** the volume slider no longer almost touches the Picture in Picture button; the gaps on the bar's right side now match the rest of the controls. The small picture's corners are rounded a little more.

## v0.38.02: Smoother Home (8 November 2026)

Home scrolls more smoothly up and down and along its rows, with a large library and with something playing in the Now Playing bar.

Your settings are all kept: none was renamed or reset.

### In short

- Home scrolls more smoothly, most of all with a large library
- Smoother still with a channel or film playing and the Now Playing bar showing
- Uses much less energy while a channel or film plays, most of all on Home

### Improved

- **Scrolling Home:** with a large library, scrolling Home up and down dropped many frames. Rows well off screen are now built only as they come near, and cards don't react to the pointer while the page is moving, so the page keeps up. A card under a still pointer lifts again as soon as the page stops.
- **Scrolling under the Now Playing bar:** the bar's small picture and its Open Now Playing button now cost less to draw over a moving page. With the bar hidden (View › Hide Now Playing Bar, ⌘/), the picture is no longer updated off screen.
- **Less energy while a channel plays:** the LIVE badge's dot still pulses, but the app no longer redraws its window for every step of the pulse, which cuts the processor use in Now Playing by about two-fifths with a channel playing. The Now Playing bar's small picture holds still while you scroll Home. With the bar hidden, or the window out of sight, the picture's frames aren't handled at all.
- **Home's banner shows its picture sooner:** the banner keeps the pictures it has shown, at the size it shows them, so after you open the app it can show the last picture straight away instead of a plain background. The first few slides' pictures are fetched first, as soon as a playlist's titles are known, and when you switch playlists the new playlist's first picture is fetched at once. A picture that has to be downloaded fades in rather than appearing suddenly.
- **Messages above the Now Playing bar:** the "Refreshing Playlist & Programme Guide…" box no longer sits behind the Now Playing bar. While the bar shows, the box appears just above it, in line with it; with the bar hidden, it's in its usual place.
- **Home while something plays:** the waveform on the playing title's Continue Watching card no longer makes the app redraw Home continuously, which took Home with a film playing from about 38% of a processor core to about 10% in testing. Home also no longer redraws its banner and every shelf each time the playing title's position is saved; only that title's card updates. The banner holds its slide while it's scrolled out of view or the window is covered, and its picture is prepared at the size it's shown.
- **Scrolling Home with a film playing:** the Now Playing bar's progress line updates on its own, at most four times a second, rather than redrawing the rest of the bar as the film plays.
- **The heart on posters:** it still shows when the pointer is on a card and always for a favourite. With VoiceOver, Add to Favourites is in the card's actions, and right-click still offers Add to Favourites.

## v0.38.01: Now Playing Bar (8 November 2026)

What's playing now sits in a floating bar at the foot of the page instead of the sidebar, leaving Now Playing shrinks the picture into it, and titles read cleanly in Now Playing and Up Next.

Your settings are all kept: none was renamed or reset.

### In short

- A floating Now Playing bar at the foot of the page replaces the sidebar's mini-player
- Leaving Now Playing shrinks the picture into the bar, and the bar opens it again
- Titles read cleanly in Now Playing and Up Next, without the quality tag, year or country

### New

- **Now Playing bar:** while something plays, a floating glass bar sits at the foot of the page, over the page itself rather than the sidebar. It has Previous, Play/Pause and Next, a small picture with the title and a thin progress line (LIVE for a channel), Mute, a volume slider and Float Video. Pages leave room at their foot for it.
- **Opening Now Playing from the bar:** click the bar's picture or title, or press ⌘0, to open Now Playing. Right-click the bar for Open Now Playing, Float Video and Close Video.
- **The picture's journey:** leaving Now Playing (Back, Esc, ⌘[ or choosing a page in the sidebar) shrinks the picture into the bar, and opening Now Playing grows it back, while the video carries on playing. With Settings › Advanced › Video › Smooth Picture Moves on, the picture moves across; with it off, or with Reduce Motion on, it fades across.
- **Show or hide the bar:** View › Hide Now Playing Bar (⌘/) hides the bar and View › Show Now Playing Bar brings it back. While it's hidden, what's playing carries on: press ⌘0 to see it.
- **Channels with the inspector open:** when the inspector shows the channel that's playing, the picture plays there and the bar shows the channel's logo.
- **Radio:** a station shows its artwork in the bar, with no Float Video button.

### Improved

- **Clean titles in Now Playing:** Now Playing and Up Next show a film's or series' title as its poster does, without the quality tag, year or country in the name: "4K-TOP - Movie Title (2024) (GB)" reads "TOP - Movie Title", or "Movie Title" with Settings › Playlists › Names & Grouping › Hide Provider Tags in Titles on. An episode reads "S1 E2 · Episode Name". The same title is used in the bar, History, Continue Watching, the window's title, the menu bar, the Dock menu and Control Centre. Before, these showed the provider's full name, with the series' name and episode code repeated.

### Removed or Moved

- **The picture in the sidebar:** the sidebar no longer has a small player at its foot; it ends at the playlist bar. What's playing is in the Now Playing bar instead.
- **The corner mini-player:** with the sidebar hidden, the small player in the window's bottom-right corner is replaced by the same Now Playing bar.

### Known issues

- **Now Playing bar:** the bar is new and has so far been tried on Home and going back from Now Playing. On other pages, with the inspector open, for radio and for Dolby Vision titles it hasn't been fully checked yet.
- **Clean titles:** checked in Now Playing so far; the bar, History, Continue Watching, window titles, the menu bar, the Dock menu and Control Centre use the same rule but haven't been fully checked yet.
- **Dolby Vision titles:** on a Mac with an Intel processor these titles still play the old way, with the notice, and so do they while casting or after you change the playback speed or the sound or subtitle timing. While one plays the new way, Save Still, Skip Intro, Up Next as the credits roll, Stream Diagnostics, Match Frame Rate, Ambient Glow, Live Captions and Picture in Picture aren't available yet, and entering or leaving full screen cuts straight across rather than gliding.
- **Subtitles on Dolby Vision titles:** styled subtitles show as plain text, and if a title has to switch to playing the old way, the subtitle track you chose isn't kept: choose it again in Subtitles.
- **Title pages:** the picture at the top of a movie's or series' page starts below the toolbar while the category list is showing, rather than running up under it as on Home.
- **Home's banner:** a title whose wide pictures all have its name lettered into them can still show the name twice.
- **Back after launch:** if the first thing you do after opening the app is play something from Home, Back doesn't return to Home. Choose Home in the sidebar instead.
- **Keychain prompts after an update:** macOS may ask for your Mac password once for each saved playlist. Choose Always Allow.
- **HDR with Smooth Picture Moves off:** HDR is shown as a standard picture.
- **Search field:** with the inspector open on Live TV and the TV Guide, the search field runs across the inspector's edge.
- **Category column:** the categories column stays at its narrow width in a larger window, so long category names are shortened.
- **Subtitles:** if subtitles don't appear, turn them off and on again.
- **External subtitle files:** a separate subtitle file from the provider (such as an .srt) isn't supported.

## v0.37.02: Dolby Vision in True Colour (7 November 2026)

Films and episodes in the Dolby Vision format that used to play with stripes and green and purple colours now play with their real colours on Macs with Apple silicon, and Home's Continue Watching cards show a wide picture instead of a cropped poster.

Your settings are all kept: none was renamed or reset.

### In short

- Dolby Vision films and episodes that showed green and purple now play in their real colours
- Long Dolby Vision episodes with many sound and subtitle tracks start, and pick up where you left off
- The colour notice shows only when a title can't play that way, and is easier to read
- Continue Watching cards show a wide picture, never a cut-off poster

### Fixes

- **Colours in some 4K HDR titles:** a film or episode in Dolby Vision profile 5 now plays with its real colours on Macs with Apple silicon, whether the provider sends it as an MKV, MP4 or MPEG-TS stream, with its sound in stereo or 5.1. Before, it showed stripes and strong green and purple colours. Pause, the timeline, skipping, Up Next, resuming where you left off, Close Video and full screen work as for any other title.
- **Long Dolby Vision episodes:** an hour-long Dolby Vision episode with many sound and subtitle tracks now starts with its picture in real colours, and resuming one you stopped part-way goes straight to the place you left it and shows the picture there. Before, resuming such an episode could leave the player waiting without a picture.
- **Dolby Vision notice:** the notice that a title's colours may look wrong no longer shows for a title that plays correctly. It shows only when the title has to play the old way, for example if its stream stops arriving, and it's now white text on the player's dark glass, easy to read.
- **Subtitles on Dolby Vision titles:** subtitles carried in the stream show on these titles, drawn over the picture.
- **Continue Watching pictures:** Home's Continue Watching cards show a wide picture: the episode's own picture, or the title's wide picture without its name lettered in, as Home's banner chooses. A title with no wide picture shows its whole poster on a soft, blurred background. Before, the card cropped the poster, cutting off its lettering and faces.

### Known issues

- **Dolby Vision titles:** on a Mac with an Intel processor these titles still play the old way, with the notice, and so do they while casting or after you change the playback speed or the sound or subtitle timing. While one plays the new way, Save Still, Skip Intro, Up Next as the credits roll, Stream Diagnostics, Match Frame Rate, Ambient Glow, Live Captions and Picture in Picture aren't available yet, and entering or leaving full screen cuts straight across rather than gliding.
- **Subtitles on Dolby Vision titles:** styled subtitles show as plain text, and if a title has to switch to playing the old way, the subtitle track you chose isn't kept: choose it again in Subtitles.
- **Title pages:** the picture at the top of a movie's or series' page starts below the toolbar while the category list is showing, rather than running up under it as on Home.
- **Home's banner:** a title whose wide pictures all have its name lettered into them can still show the name twice.
- **Back after launch:** if the first thing you do after opening the app is play something from Home, Back doesn't return to Home. Choose Home in the sidebar instead.
- **Keychain prompts after an update:** macOS may ask for your Mac password once for each saved playlist. Choose Always Allow.
- **HDR with Smooth Picture Moves off:** HDR is shown as a standard picture.
- **Search field:** with the inspector open on Live TV and the TV Guide, the search field runs across the inspector's edge.
- **Category column:** the categories column stays at its narrow width in a larger window, so long category names are shortened.
- **Subtitles:** if subtitles don't appear, turn them off and on again.
- **External subtitle files:** a separate subtitle file from the provider (such as an .srt) isn't supported.

## v0.37.01: New Film and Series Pages (7 November 2026)

Movie and series pages open with the title's wide picture and its details, as Home's banner does, with a series' episodes from every season in one row and the title's other details below; a video you closed no longer plays again at launch.

Your settings are all kept: none was renamed or reset.

### In short

- Movie and series pages open with the title's wide picture and details, as on Home
- A series' episodes run in one row across every season, with the Season menu following along
- Related, Cast & Crew, About and Information below, where the provider lists them
- A video you closed before quitting no longer plays again at launch

### New

- **Movie and series pages:** a title's page now opens with its wide picture, sharp and in its own shape, as Home's banner shows it, with the title, its type, genres and age rating, a two-line description with More for the rest, the year, running time and rating, then Play (or Resume), Trailer, the version picker, Favourite and Download. Share is in the toolbar. The title shows in the toolbar once you scroll past the picture. Before, the page's top was a heavily blurred picture.
- **Below the picture:** the page goes on with Related titles, Cast & Crew (shown with their initials), About (the genres and the full description) and Information (released, running time, age rating, country and director). Anything the provider doesn't list is simply left out.
- **Episodes in one row:** a series' episodes from every season run in one row, in order, so season 2's first episode follows season 1's last. Each card shows the episode's picture, its number, title, three lines of description and running time, and, where you've started it, how far you got; its menu has Play, Mark as Watched (or Unwatched) and Download where available.
- **Season menu:** the Season menu above the row follows it: as the row scrolls into a season, the menu shows that season, and choosing a season moves the row there.
- **Notice for one HDR format:** a title whose provider says it uses Dolby Vision profile 5 now says, on its page and over the picture as it starts playing, that its colours may look wrong, as the app can't show that format yet. Nothing else about playing it changes.

### Improved

- **First load:** while the app fetches the TV Guide on its first load, it now says "Guide for the first 200 channels; the rest loads as you browse", and a Continue button lets you start using the app straight away, while the guide carries on loading. Before, it read as if those were all your channels, and there was no way past that step.

### Fixes

- **First-load percentage:** the percentage on the first-load screen counts up cleanly. Before, its digits could look broken while they changed.
- **Resume at launch:** with Settings › General › Startup › Resume Last Channel on Launch on, a live channel plays again at launch only if it was still playing when you quit. A film or episode playing when you quit leaves nothing playing at launch. Before, the last channel played again even after you'd closed it, or while a film was playing.

### Known issues

- **Colours in some 4K HDR titles:** a 4K HDR episode or film in one particular Dolby Vision format can show strongly wrong colours. The app now says so on its page and in the player, but doesn't support that format yet.
- **Title pages:** the picture at the top of a movie's or series' page starts below the toolbar while the category list is showing, rather than running up under it as on Home.
- **Home's banner:** a title whose wide pictures all have its name lettered into them can still show the name twice.
- **Back after launch:** if the first thing you do after opening the app is play something from Home, Back doesn't return to Home. Choose Home in the sidebar instead.
- **Keychain prompts after an update:** macOS may ask for your Mac password once for each saved playlist. Choose Always Allow.
- **HDR with Smooth Picture Moves off:** HDR is shown as a standard picture.
- **Search field:** with the inspector open on Live TV and the TV Guide, the search field runs across the inspector's edge.
- **Category column:** the categories column stays at its narrow width in a larger window, so long category names are shortened.
- **Subtitles:** if subtitles don't appear, turn them off and on again.
- **External subtitle files:** a separate subtitle file from the provider (such as an .srt) isn't supported.

## v0.36.06: Fuller Banner, Steadier Picture (7 November 2026)

Home's banner shows a title's wide picture in its own shape with faces in view, with the title's details over it; going back from Now Playing, the picture moves straight to its place; and posters show a quality tag as a small badge.

Your settings are all kept: none was renamed or reset.

### In short

- Home's banner shows the picture in its own shape, keeping faces in view
- The banner lists genres, running time, credits and quality, with Play, Details and Favourite
- Back from Now Playing, the picture goes straight to its place
- Posters show a quality tag such as 4K as a small badge

### New

- **Home's banner details:** the banner now shows, at the bottom left, the title, its type, genres and age rating, a two-line description with More for the rest, the year, running time, rating and quality, then Play, Details and a Favourite button. Wider windows show who stars in it and who directed it at the bottom right. Anything the provider doesn't list is simply left out.
- **Quality badges on posters:** a quality tag at the start of a movie's or series' name, such as 4K or UHD, shows as a small badge beside the title on its poster, whether or not Settings › Playlists › Names & Grouping › Hide Provider Tags in Titles is on. Where the quality is joined to another tag, as in “4K-TOP - Movie Title”, the badge shows 4K and the name keeps “TOP - ” unless that setting is on.

### Fixes

- **Home's banner picture:** the banner takes the shape of a title's wide picture, getting taller as the window gets wider, but never more than a little over half the window, so the first row below always shows. Where it has to trim the picture, it keeps faces in view, or the upper part of the picture where there are none. Before, it showed only a thin strip across the middle, and heads could be cut off.
- **Home's banner text:** the title and buttons read through a soft shade rising from the bottom-left corner, only as strong as the picture behind them needs: light over a dark picture, stronger over a bright or busy one. Before, a blurred box sat behind them and could blur across a face.
- **Going back from Now Playing:** with Smooth Picture Moves on, going back from Now Playing to a movie's or series' page, the picture moves once, straight into its place on the page. Before, it swung left and then back right before settling.
- **Home's banner page dots:** the dots at the bottom right show on one clear glass capsule again. Before, they could look broken over a busy picture.

### Known issues

- **Home's banner:** a title whose wide pictures all have its name lettered into them can still show the name twice.
- **Back after launch:** if the first thing you do after opening the app is play something from Home, Back doesn't return to Home. Choose Home in the sidebar instead.
- **Keychain prompts after an update:** macOS may ask for your Mac password once for each saved playlist. Choose Always Allow.
- **Colours in some 4K HDR titles:** a 4K HDR episode or film in one particular HDR format can show strongly wrong colours. The app doesn't support that format yet.
- **HDR with Smooth Picture Moves off:** HDR is shown as a standard picture.
- **Search field:** with the inspector open on Live TV and the TV Guide, the search field runs across the inspector's edge.
- **Category column:** the categories column stays at its narrow width in a larger window, so long category names are shortened.
- **Subtitles:** if subtitles don't appear, turn them off and on again.
- **External subtitle files:** a separate subtitle file from the provider (such as an .srt) isn't supported.

## v0.36.05: Cleaner Banner and HDR Films (7 November 2026)

Home's banner shows a title's picture edge to edge, as it is, with no dark shading, and prefers a picture without the name lettered into it; HDR films start with Smooth Picture Moves on.

Your settings are all kept: none was renamed or reset.

### In short

- Home's banner: no dark shading, and no doubled name where the provider has a clean picture
- HDR films start with Smooth Picture Moves on

### Fixes

- **Home's banner:** the banner shows a title's picture as it is, running edge to edge and up under the toolbar and sidebar, with no dark fades and a clean edge where the page begins. The picture is no longer moved up or down. Where the provider has several wide pictures for a title, the banner shows the first one without the name lettered into it, so the name isn't shown twice. The title and buttons read through a soft blur behind them only. Before, a moved picture could put its own lettering behind the title, or leave a flat band under the toolbar.
- **HDR films:** an HDR film now starts and plays in HDR with Smooth Picture Moves on. Before, it stopped with an error a moment after starting.

### Known issues

- **Home's banner:** a title whose wide pictures all have its name lettered into them can still show the name twice.
- **Keychain prompts after an update:** macOS may ask for your Mac password once for each saved playlist. Choose Always Allow.
- **Colours in some 4K HDR titles:** a 4K HDR episode or film in one particular HDR format can show strongly wrong colours. The app doesn't support that format yet.
- **HDR with Smooth Picture Moves off:** HDR is shown as a standard picture.
- **Search field:** with the inspector open on Live TV and the TV Guide, the search field runs across the inspector's edge.
- **Category column:** the categories column stays at its narrow width in a larger window, so long category names are shortened.
- **Subtitles:** if subtitles don't appear, turn them off and on again.
- **External subtitle files:** a separate subtitle file from the provider (such as an .srt) isn't supported.

## v0.36.04: Clearer Guide and Banner (6 November 2026)

Long channel names now read in the TV Guide, Home's banner keeps a title's lettering in view, and every play button over a card or poster is the same amber.

Your settings are all kept: none was renamed or reset.

### In short

- Long channel names readable in the TV Guide
- Home's banner keeps the title in its picture in view
- One amber play button on every card and poster

### Fixes

- **TV Guide channel names:** a long name now shows its first 20 or so characters. Before, a channel with HD and HD HEVC versions showed only the first few letters of its name, because the version labels took the room. The labels now step aside when the name needs the room (choose a version from the channel's menu), and the channel column is a little wider.
- **Home's banner:** when a title's wide picture has its name lettered into it, the banner now moves the picture so the lettering shows, whether it sits near the picture's top, middle or foot. Before, lettering near the top or foot could be cut off.
- **Play buttons:** the play button that appears over a card or poster under the pointer is the same amber button everywhere: Home's On Now and Continue Watching cards, posters, radio stations, and a channel's picture in Live TV before it plays. Before, some were grey glass.

### Known issues

- **Keychain prompts after an update:** macOS may ask for your Mac password once for each saved playlist. Choose Always Allow.
- **Some HDR films may not start** with Smooth Picture Moves on.
- **Colours in some 4K HDR titles:** a 4K HDR episode or film in one particular HDR format can show strongly wrong colours. The app doesn't support that format yet.
- **HDR with Smooth Picture Moves off:** HDR is shown as a standard picture.
- **Search field:** with the inspector open on Live TV and the TV Guide, the search field runs across the inspector's edge.
- **Category column:** the categories column stays at its narrow width in a larger window, so long category names are shortened.
- **Subtitles:** if subtitles don't appear, turn them off and on again.
- **External subtitle files:** a separate subtitle file from the provider (such as an .srt) isn't supported.

## v0.36.03: HDR in Full Colour (6 November 2026)

HDR channels now use your display's full brightness and colour with Smooth Picture Moves, in Live TV's inspector, Now Playing, full screen and the floating window.

Your settings are all kept: none was renamed or reset.

### In short

- HDR channels in full brightness and colour
- HDR found on channels sent as a plain stream

### Fixes

- **HDR:** with Smooth Picture Moves on (Settings › Playback), an HDR channel in Live TV's inspector, Now Playing, full screen or the floating window uses the full brightness and colour of a display that supports HDR. Before, it looked dull and washed out. Standard channels look exactly as before.
- **HDR channels sent as a plain stream:** these are now recognised as HDR. Before, they played as a standard picture.

### Known issues

- **Keychain prompts after an update:** macOS may ask for your Mac password once for each saved playlist. Choose Always Allow.
- **Some HDR films may not start** with Smooth Picture Moves on.
- **Colours in some 4K HDR titles:** a 4K HDR episode or film in one particular HDR format can show strongly wrong colours. The app doesn't support that format yet.
- **HDR with Smooth Picture Moves off:** HDR is shown as a standard picture.
- **Search field:** with the inspector open on Live TV and the TV Guide, the search field runs across the inspector's edge.
- **Category column:** the categories column stays at its narrow width in a larger window, so long category names are shortened.
- **Subtitles:** if subtitles don't appear, turn them off and on again.
- **External subtitle files:** a separate subtitle file from the provider (such as an .srt) isn't supported.

## v0.36.02: Episodes and the Inspector (6 November 2026)

Episodes now move on only after one has really played to its end, Live TV's inspector and the small players are tidier, and preferred subtitle languages are matched better.

Your settings are all kept: none was renamed or reset.

### In short

- Autoplay no longer skips through several episodes
- No black bars or thin dark line on Live TV's inspector picture
- Small players' controls centred, with Play/Pause in the middle
- Subtitle languages matched by three-letter codes
- One Just Finished card per programme in Catch-Up

### Fixes

- **Episodes:** the next episode starts only after an episode has played to its end, and only once. Before, an episode that failed or ended at once counted as finished, so autoplay could run through several episodes. An episode that never plays now shows the player's error and stays; one that stops partway says so. A saved place at or past the end starts the episode from the beginning.
- **Live TV's inspector picture:** a standard-definition channel sent as 16:9 or 4:3 fills its frame instead of sitting between black bars above and below. With Smooth Picture Moves on, a thin dark line along the top of the picture is gone.
- **Small players:** the controls in the Live TV inspector and the other small players are centred in the picture, with Play/Pause in the middle, and the PLAYING label is hidden while the controls show.
- **Small players, narrow inspector:** where Expand doesn't fit beside a catch-up channel's LIVE button, it moves to a second row.
- **Subtitle and audio language:** a preferred language now matches tracks the stream names by three-letter code (such as "eng" or "ger"), so the subtitles you prefer are picked.
- **Catch-Up:** Just Finished shows one card per programme across a channel's HD and 4K versions (with Group Channel Versions on).

### Known issues

- **Keychain prompts after an update:** macOS may ask for your Mac password once for each saved playlist. Choose Always Allow.
- **Colours in some 4K HDR titles:** a 4K HDR episode or film in one particular HDR format can show strongly wrong colours. The app doesn't support that format yet.
- **Subtitles:** if subtitles don't appear, turn them off and on again.
- **External subtitle files:** a separate subtitle file from the provider (such as an .srt) isn't supported.

## v0.36.01: A New Look (6 November 2026)

Home, the TV Guide and Live TV have a new, calmer look, the picture goes straight to its place when it moves, and the
TV Guide copes better with slow providers.

Your settings are all kept: none was renamed or reset. One new choice starts with a default: the TV Guide shows the
channels that have a guide until you pick All Channels in Category, which it then remembers.

### In short

- A new Home, with a banner of new films and series
- A calmer TV Guide that shows the channels with a guide
- Live TV rows with what's on next, and an inspector beside the list
- Search results grouped by kind
- The picture goes straight to its place when it moves
- Category names on one line

Some controls have moved; the full notes say where.

### New

- **Home:** a banner across the top of the page shows new films and series one at a time, with its colour carried softly under the sidebar and toolbar. Play, Details or View Series are on it; the arrows to step through appear when you point at the banner (they also work from the keyboard and with VoiceOver). Its foot fades softly into the page, and a title shows without the year and country codes some providers add after it. Below it, Continue Watching, On Now, Recently Added Films and Favourite Channels. The two new sections can be moved or hidden in Settings › Appearance › Home.
- **TV Guide:** quieter programme cells, today opening with the current time a third of the way across, and a red line for now. The TV Guide shows the channels that have programme information; the bar says how many don't, and Category › All Channels in Category shows them all. A channel without a guide says so, and clicking it plays the channel; one whose guide turns out to be empty is left out, and counted, the next time you open its category. With a channel playing, the inspector shows it and its programme is highlighted, so the picture stays in the inspector when you come from Live TV. The TV Guide remembers the category you chose for each playlist, even after you quit.
- **Live TV:** each row shows the channel, what's on now with its progress, and "Next: … at …" where there's room. The inspector beside the list shows the channel playing, with its colours glowing softly around the picture, in the picture's own shape (a 4:3 or SD channel has no bars at its sides); with nothing playing it shows the channel's logo on a soft wash of its colours.
- **Channel logos:** a channel without a logo gets a coloured tile with its initials.
- **Search:** results are grouped by kind (All, Channels, Radio, Movies, Series), each with its count, and Show All lists one kind in full.

### Changed

- **Posters:** Movies and Series show smaller posters, so more titles fit: four or five to a row where there were three at the same width. More Like This keeps its size.
- **Backgrounds:** pages sit on the Mac's own window background, in Light and Dark.
- **Sign-in and loading screens:** the splash, signing in, the playlist chooser and the first load share one layout, so the logo stays in one place as you go from one to the next.
- **Sidebar:** keeps the same width at every window size; it used to narrow in a smaller window.
- **Catch-Up:** its column matches the other pages, with icons, counts, a filter field and country headings.
- **Small players:** the mini player and Live TV's inspector share one compact set of controls on a single row, chosen by the player's size; the mini player's controls cover less of the picture.
- **Volume:** the volume slider stays on the player bar, narrowing in a small window rather than disappearing. In the floating window and Live TV's inspector, the speaker button opens a slider.
- **Player controls:** they stay on screen while the pointer rests on them, and hide again once you move away.
- **TV Guide loading:** a guide request that stalls gives up sooner (it used to wait up to two minutes), so one slow reply no longer holds up the other channels' guides.
- **Rewind 1 Minute** works on a live channel that keeps a catch-up archive even when it has no guide.

### Removed or Moved

- **Live TV's Show, Sort By and Find a Channel:** now in the toolbar's View Options menu.
- **Live TV's page header:** the All Channels title, the channel count and the filter row are gone; the window's title names the page.
- **The heart on Live TV rows:** right-click a channel and choose Add to Favourites, or click Favourite in the inspector.
- **Time left in Live TV rows:** still shown in the inspector.
- **The TV Guide's category column:** with its filter field and right-click menu, it's replaced by the Category menu at the top of the TV Guide.
- **The TV Guide's All, Favourites and Catch-Up buttons:** now Show, at the top of the Category menu, with Pin to Sidebar.
- **Channel numbers in the TV Guide:** the channel column shows the logo and name only.
- **Home's See All:** your favourites are on the sidebar's Favourites page.
- **The NEW MOVIE and NEW SERIES badge** on Home's banner is gone.

### Fixes

- **Picture moves:** the picture goes straight to its place when it moves into Now Playing, from full screen, the mini player, the floating window or a title's page. Before, it drifted to one side and then settled.
- **Ambient Glow:** the light beside each edge of the picture is the colour the picture has there. Before, a bright edge in Now Playing could have a dark band beside it.
- **Title pages:** a film's or series' artwork fades smoothly into the page. Before, it ended in a hard line with a brighter band below it.
- **Category names:** each category is on one line in every section, with its full name in its tooltip. Where quality tags tell two categories apart, the tags give way before the name. Before, long names wrapped to two lines and crowded the list.
- **Black bars in Now Playing and full screen:** the picture keeps one size through a film or episode. Before, a dark scene could crop into the picture, and its size changed again as the scene lightened.
- **Movie years:** cards show the year a film came out, or none, rather than the year your provider added it.
- **Playback menu:** Start from Beginning and Rewind 1 Minute are there on a live channel whose programme is in its catch-up archive. Before, Rewind was always greyed out in the menu.
- **TV Guide times:** with providers that don't send their server's time, programmes no longer show late.
- **TV Guide:** a channel without a guide no longer says "Loading guide…" for minutes.
- **Catch-Up:** its preview pictures no longer load in the background while something is playing.
- **Leaving full screen:** the app no longer quits now and then as the picture returns to the window, with Smooth Picture Moves turned off.
- **Window subtitle:** a playlist added without a name shows as "Playlist" rather than its server's address.

### Known issues

- **Energy:** Now Playing uses more energy than it should. This is still being worked on.
- **HDR:** some live HDR channels play in standard range.
- **Reopening the app:** with Resume Last Channel on Launch on (Settings › General), the last channel plays again even if you closed the video before quitting.
- **Sidebar:** the selected row is grey rather than your accent colour.

## v0.35.03: Pins and Menus (3 November 2026)

Pinned categories open the category you pinned, the player's controls stay up while one of its menus is open, and
Live TV scrolls more smoothly.

### Fixes

- **Pinned categories:** clicking a pin in the sidebar opens its category even when you're already in that section. Before, it stayed on the category you were looking at.
- **Sidebar highlight:** the sidebar highlights the pin whose category is showing, and goes back to the section when you choose another category. Before, the section stayed highlighted, and clicking it didn't take you off the pinned category.
- **Player menus:** while a player menu is open (Subtitles, More, or the menu on a stream's status), the controls and the close button stay on screen, in every player and in full screen. Once it closes, whether you choose an item, press Escape or click elsewhere, they hide again as usual. Before, they could hide under an open menu, or stay up for good after Escape.
- **Opening the app:** no moving amber glow flashes behind the loading screen when the app signs in with a saved login, or behind "Signing in…".
- **Live TV:** scrolling the channels stutters less while their programme information comes in.

Your settings are all kept: none was renamed or reset.

## v0.35.02: Smooth Scrolling (2 November 2026)

Live TV, Movies and Series scroll smoothly however large your library is, and the pages look more like the rest of
the Mac.

### Changed

- **Smooth scrolling:** Live TV's channels and the Movies and Series grids scroll without stutter, even with tens of thousands of titles. Showing and hiding the sidebar is smoother too.
- **Live TV:** every channel row is the same height, with its columns lined up: the channel, what's on now (in bold, with its progress) and "Next: Programme at 21:00". Click a channel or move with ↑ / ↓ to show it in the inspector; double-click or press Return to play it.
- **Movies and Series:** larger posters, with each title's year shown once, and the right number of columns at every window width. Click a poster to select it, move with the arrow keys, and double-click or press Return to open it.
- **Movie and series pages** open on a band of the title's artwork, with Play and its details over it; a series switches seasons with a segmented control, and More Like This follows below.
- **TV Guide:** a Day pop-up beside Now, a red line and time for now, a narrower channel column, and ↑ / ↓ and Return to move through the channels and play.
- **Sidebar mini player:** just skip back, Play/Pause, skip forward and Expand, with the close cross.
- **Favourites and History** filter by kind with a segmented control at the top of the page.
- **Categories** have an icon each, and Hide Country Prefixes also drops a leading section word ("Movies - Drama" shows as "Drama").
- **Search:** the toolbar's search field sits in the inspector's part of the toolbar when the inspector shows, and says what it finds (channels, radio, movies and series). Each page's find field is the Mac's own search field.
- The sidebar's footer is just the playlist menu, and Home's banner says Details.

### Fixed

- Live TV rows show what's on now again; on a narrow window it had been squeezed to nothing.

Your settings are all kept: none was renamed or reset.

## v0.35.01: A Mac Window (1 November 2026)

ElBee Player's window is laid out as Apple's own apps lay theirs out: a sidebar of sections, a column of categories,
the page, and an inspector.

### New

- **Sidebar:** Home, Recently Added, Live TV, TV Guide, Catch-Up, Radio, Movies, Series, Favourites and History sit in the sidebar under Watch and Library, with your pinned categories, on the Mac's own selection and glass. The section tabs in the toolbar are gone.
- **Categories column:** each section's categories (or Catch-Up's channels, or a kind filter for Favourites, History and Recently Added) in a column of their own beside the sidebar, with a Filter Categories field and each category's count. Movies and Series start with All Movies and All Series, as Live TV starts with All Channels, and every count matches its page.
- **Inspector:** the channel or programme you pick in Live TV or the TV Guide shows at the window's right edge: its picture or artwork, what's on now and next, catch-up, Play and Favourite. The toolbar's Inspector button shows and hides it, and it's remembered. In a narrow window it steps aside, as Apple's inspectors do, and comes back when there's room.
- **Search:** the Mac's own search field in the toolbar, with suggestions of the first matches as you type. ⌘F puts the cursor there.

### Changed

- **One window:** no New Window and no tabs, and the window is no longer maximised at launch. Its size, place and sidebar width carry over from before.
- **Now Playing** takes two columns, the sidebar and the player, and the window's title says Now Playing.
- **Home's banner** takes about a third of the window, and with Reduce Motion on it stays on its title until you pick another.
- **Sign in, Choose a Playlist and the first library load** are plain pages on the window, as the Mac's own setup screens are.
- The Spotlight banners above Live TV and the TV Guide are replaced by the inspector; their settings are now Channel Inspector and Programme Inspector.
- **Times** follow your Mac's clock: 00:35 on a 24-hour Mac, 12:35 AM on a 12-hour one.
- Posters, Catch-Up programmes, On Now tiles and the pictures that open Now Playing are buttons that VoiceOver and Full Keyboard Access reach.
- A channel card's logo has corners that follow the card's.

### Fixed

- **Share** sends a title's words and picture as one item, so the share menu no longer says "2 Images".
- **Settings:** under keyboard focus the tabs say their names, not their symbols'.

Your settings are all kept: none was renamed or reset.

## v0.34.01: At Home on the Mac (1 November 2026)

ElBee Player works with the rest of your Mac: the Dock, the menu bar, Control Centre, Share and Quick Look.

### New

- **Dock menu:** right-click ElBee Player in the Dock for what's playing, Play/Pause, Next and Previous, and your favourites.
- **Menu bar:** Settings › General › Show in Menu Bar puts ElBee Player at the right of the menu bar, with what's playing, Previous, Play/Pause and Next, and your favourites. It's off unless you turn it on.
- **Share** a programme from the player's More menu, or a movie or series from its page: its name, its time and its artwork. Never a stream address.
- **Downloads & Recordings** (Library menu, ⌥⌘L) lists what you've downloaded and recorded. Press Space for Quick Look, as in Finder.

### Changed

- **Control Centre** shows the programme on now for a live channel, with the channel under it, and you can drag its position bar to move through a movie or episode. A radio station plays as sound.
- **Media keys** belong to ElBee Player only while something is open in the player; with nothing open they go back to the app that played last.
- **A paused player rests:** paused in Now Playing or full screen, ElBee Player uses close to no processor time.
- **Settings:** the six tabs sit centred at the top on their own, with search under them. Settings opens with nothing selected; ⌘F puts the cursor in the search field.
- A movie or series picked from the Dock, the menu bar or Spotlight opens on its page even while Now Playing is up.

### Fixed

- **Parental lock:** locked categories stay out of Spotlight, the Dock menu and the menu bar while the lock is on.
- **Quit** works while What's New or setup is open: the sheet closes and the app quits.
- **Categories:** dragging a category that isn't selected moves only that one; a click on the list lets the arrow keys move through it; the first drag works straight away.
- **Setup's Categories step** scrolls once, not a list inside a scrolling page.

Your settings are all kept: none was renamed or reset.

## v0.33.01: Settings, the Mac Way (1 November 2026)

Settings is rebuilt as a standard Mac settings window, with six tabs along the top, and your playlists and categories are managed there.

### Changed

- **Six tabs:** General, Playlists, Playback, Live TV, Appearance and Advanced, along the top of the Settings window, each one page of grouped settings. Settings opens on the tab you used last, the window can be resized and keeps its size, and each tab has its own Restore Defaults.
- **Search** sits in the Settings window's toolbar (⌘F); a result opens its tab and lights up the setting.
- **Long descriptions** open from a help button beside the setting, so the pages stay short.
- **Playlists in Settings:** Settings › Playlists lists every playlist beside its details, in place of the Manage Playlists window: add with +, remove with −, more in the ••• menu, Check All under the list, and Switch to This Playlist and Refresh Library Now on the page. Edits you haven't saved are asked about before you move to another playlist or tab. **Sign In Automatically To** moves here from General.
- **Categories in Settings:** Manage Categories… (⇧⌘K) opens a page of the Playlists tab. Its categories are a list: select several to show or hide them at once, drag to reorder, and right-click for Move to Top, Move Up, Move Down, Move to Bottom and Reorder Channels…
- **What's New and setup open as sheets** on the main window, as in Apple's apps, with the same Categories list in setup as in Settings.
- **About ElBee Player** is the Mac's own About window (ElBee Player › About ElBee Player).

Your settings are all kept: none was renamed or reset.

## v0.32.03: Glass All Around (1 November 2026)

The last frosted panels over the picture move to clear glass, and Live TV, Radio, Multi-View and Home follow Apple's glass more closely.

### Changed

- **The connection card and Stream Diagnostics use clear glass:** Reconnecting, Connection Lost and the small capsule on little pictures, and Stream Diagnostics, now sit on the same clear glass as the controls, with white text, and the picture dims behind them while they show, even with the controls hidden.
- **Live TV's Channel Spotlight:** Watch, Start from Beginning and the other buttons there are glass buttons, alongside the heart and Record.
- **Radio's genres** are the Mac's own segmented control, with no band behind them; the genres, sort and find now scroll with the stations.
- **Multi-View** dims each picture under its glass while the pointer is over it, as the other players do, and an empty slot shows its + on clear glass over the window.
- **Home's arrows and the Radio player's station logo** sit on clear glass over the artwork.

### Fixed

- **Leaving full screen** no longer makes the controls flicker in Now Playing when the pointer is still: they stay as they were in full screen.

## v0.32.02: Clear Glass Everywhere (1 November 2026)

Full screen now uses the same clear glass as Now Playing, so the player looks the same in every state.

### Changed

- **Full screen uses clear glass:** in place and in a full-screen Space, the controls, Up Next and Skip Intro sit on the same clear glass as in Now Playing, the mini player and the floating window, with the picture dimmed behind them, the same in Light and Dark. The connection card and Stream Diagnostics keep their frosted glass, so their text stays easy to read.

## v0.32.01: Native Glass (1 November 2026)

The player's controls now sit on the Mac's own Liquid Glass, as Apple's apps do: clear over the picture, which dims behind them, and Skip Intro and Up Next grow out of the control bar and melt back into it.

### In short

- Clear glass over the picture, with white controls, the same in Light and Dark
- The picture dims behind the controls while they show
- Skip Intro and Up Next grow out of the control bar, side by side
- The controls hide 2 seconds after the pointer stops (it was 3)

### Changed

- **The player's glass is the system's own:** in Now Playing, the mini player, the floating window and the banners, the controls sit on clear glass with white glyphs, the same in Light and Dark; the full-screen player uses the system's regular glass, and its window stays dark while it shows. Neighbouring glass shares one layer, so pieces blend as they come and go rather than fading.
- **The controls hide 2 seconds after the pointer stops** (it was 3), and fade in and out in about 0.2 seconds, as in Apple's own player.
- **Reduce Transparency and Increase Contrast** on the player's and the pages' glass are now drawn by macOS itself, the way Apple's apps show them; the glyphs stay white.

### New

- **The picture dims behind the controls** while they show, so they read over any picture, and brightens again as they go.
- **Skip Intro and Up Next grow out of the control bar** and melt back into it. If both show, they sit side by side on the bar's right edge; whichever came first keeps its place, and neither moves while the pointer is over the controls.
- **Channel Spotlight's Record button** grows out of the heart as the preview starts, and the Radio banner's controls and heart share one piece of glass.

### Improved

- **The connection card and Stream Diagnostics** sit on frosted glass, so their text reads over a bright or colourful picture.
- **Entering and leaving full screen:** the controls and the dimming stay up through macOS's animation, in place and in a full-screen Space, then hide as usual.
- **Space and the Live TV spotlight's arrow keys** no longer take keyboard focus away from the controls: a button you reach with Tab keeps Space, and a search field keeps its typing.
- **Multi-View's "Add Channel"** label is easier to read in Light Mode.

## v0.31.01: Menus and Shortcuts (31 October 2026)

ElBee Player's menus now cover everything the app does, with the shortcuts you'd expect from a Mac app, and Back and Forward take you through where you've been.

### In short

- A fuller menu bar: Go To each section, Back and Forward, Hide Toolbar, and more playback controls
- Right-click menus start with Play, and offer Show in Guide, Download and Mark as Watched
- New shortcuts for subtitle timing: ⌃⌘[ and ⌃⌘] (⌘[ and ⌘] now go back and forward)
- Menus with nothing to choose are greyed out

### Changed

- **Subtitle timing has new shortcuts:** **Subtitles Earlier** is now **⌃⌘[** and **Subtitles Later** is **⌃⌘]** (they were ⌘[ and ⌘]). They've moved from the View menu to **Playback › Subtitle Timing**, beside Sound Timing. ⌘[ and ⌘] now go back and forward, as in other Mac apps.

### New

- **A fuller menu bar:**
  - **View** has **Now Playing** (⌘0), **Go To** each section (⌘1 Home to ⌘8 Recently Added), **Back** and **Forward** (⌘[ and ⌘], through the sections, pages and Now Playing you've visited), **Hide Toolbar** (⌥⌘T), **Show Sidebar** (⌃⌘S) and **Keep Window on Top**.
  - **Playback** adds **Play/Pause**, **Rewind** and **Skip Forward**, **Jump to Live** (⌘J), **Volume Up** and **Down** (⌘↑ and ⌘↓), **Mute** (⌥⌘↓), **Subtitles** and **Record**.
  - **Library** adds **Refresh All** (⌘R), **Refresh Category** (⌥⌘R), **Add to Favourites** (⌘D) and **Show in Guide** for what's playing.
- **Fuller right-click menus:** channels, stations, movies and series now start with **Play** (a series: **Show Episodes**), and offer **Show in Guide** (channels), **Download** and **Mark as Watched** (movies) alongside Play in Multi-View, Favourites, Show Details and Hide. A channel in the TV Guide has the same menu.
- **Show in Guide** opens the TV Guide with that channel chosen and in view.

### Improved

- **Menus that have nothing to choose are dimmed:** in the Playback menu and the player's **More** and **Subtitles** menus, Speed, Sound Timing, Subtitle Timing, Sleep Timer, Subtitles and Deinterlace Mode are greyed out when nothing in them can be chosen (for example Speed on a live channel), instead of opening onto a list of greyed-out items.
- **Multi-View** is listed once in the Window menu, with ⇧⌘M.

## v0.30.01: Your Colours, Clearer Glass (31 October 2026)

ElBee Player now uses the accent colour you chose for your Mac, and the controls over a picture stay easy to read in Light Mode and with the accessibility display settings.

### In short

- Your Mac's accent colour, everywhere in the app (amber stays under Multicolour)
- Controls over a picture are dark and readable in Light Mode too
- In Dark Mode, the glass behind the player's controls is a little darker than before
- Reduce Transparency, Increase Contrast, Reduce Motion and Differentiate Without Colour are followed throughout

### Improved

- **Your accent colour:** buttons, switches, selected rows, focus rings and highlights now follow the accent colour chosen in **System Settings › Appearance**. Golden amber is still ElBee Player's own colour, and shows when your accent is set to **Multicolour**; it's a little deeper in Light Mode and with **Increase Contrast**, so it stays readable. Play buttons, progress bars and the logo keep their amber.
- **Controls over a picture:** the control bar, the close button, badges and messages over a video could turn pale under their white text: always in Light Mode, and in Dark Mode over a bright picture. They're now dark glass in every player and either appearance. **You'll notice this in Dark Mode too:** the glass behind the controls, badges and messages over a video is a little darker than before, so it reads well over bright pictures and looks the same as in Light Mode.
- **Reduce Transparency:** with it on (**System Settings › Accessibility › Display**), the control bar, cards and buttons over a picture or a page are solid instead of glass. **Plain Look** (Settings › Appearance) is greyed out meanwhile, since it would make no difference.
- **Increase Contrast:** glass panels and buttons get a clear outline.
- **Ambient Glow:** it rests while Reduce Transparency, Reduce Motion or Increase Contrast is on, and comes back when they're off. Its switch in Settings and in the player's **More › Video** menu reads Off and is greyed out meanwhile, saying why. Your own setting is kept.
- **Differentiate Without Colour:** with it on, nothing is shown by colour alone. For example, the toolbar's Now Playing button fills in while Now Playing is open, Radio's chosen genre and a channel's preferred version show a checkmark, and Stream Diagnostics shows a warning sign while a stream struggles.
- **Window background:** the **Window Background Opacity** slider (Settings › Appearance) is gone. In Dark Mode the window always uses the standard background, as solid as the slider's default; if you had lowered it, the window is now less see-through.
- **Catch-up icon:** programmes you can watch from catch-up, and **Watch from Catch-Up**, now use a clock icon instead of the rewind arrow, so they can't be mistaken for Skip Back.

## v0.29.02: Closing in Full Screen (30 October 2026)

The close button works again in full screen.

### Fixes

- **Closing a video in full screen:** the close button (×) only brought up the controls. It now closes the video.

## v0.29.01: Next and Previous (30 October 2026)

Step to the next or previous channel, station or episode from the player, the menu bar or your keyboard, with the same controls in every size of player.

### In short

- Next and Previous for channels, stations and episodes (⌘→ / ⌘←, or your media keys)
- Previous Channel is now called Last Watched Channel (⌘L)
- Live Captions now match subtitles in size
- The same controls in every player, from the mini-player to full screen

### New

- **Next and Previous:** every player has Previous and Next buttons either side of the play controls, named for what's playing (Next Channel, Previous Episode, Next Movie). Channels and stations follow the list you're looking at, with its category, filter, search and sort, and go round from the last to the first. A channel that isn't in that list goes to the nearest one that is, and before you've opened a list they go through all your channels. Episodes go through the series and stop at the first and last. For a movie, Next plays what's queued. While you're recording they don't switch, and the player says why.
- **Next and Previous from the keyboard:** **Playback › Next** (⌘→) and **Playback › Previous** (⌘←), your keyboard's media keys and Control Centre do the same, with **Use Media Keys & Control Centre** on (Settings › General › System). While you're typing in a search or text field, ⌘← and ⌘→ move to the start and end of the line as usual.
- **Next and Previous on the radio:** the radio player has **Previous Station** and **Next Station** either side of Play/Pause.
- **More in the More menu:** the player's **More** button now also has **Play in Multi-View** (on a channel), **Stream Diagnostics** (⌘I) and **Close Video**.
- **When it ends, and which quality:** above the timeline, a live channel shows when its programme ends ("Ends 21:30"). A programme from the archive says **Behind Live** or **Catch-Up**, with how far in you are and its name. A movie or series that comes in several qualities shows which one is playing ("4K").

### Improved

- **Last Watched Channel:** **Playback › Previous Channel**, which goes back to the channel you were watching before, is now called **Last Watched Channel** (⌘L). It works as before.
- **Live Captions:** they now grow and shrink with the picture, as subtitles do, so at the same size the two match in every player, full screen included. Your **Live Caption Size** (Settings › Playback › Subtitles & Captions) is kept.
- **Subtitles menu:** it's named for what's playing ("Subtitles from the Movie"), with Off and each subtitle track in one list, then **Subtitle Timing**. Its button fills in while subtitles or Live Captions are on.
- **Start from Beginning:** a new icon, a circular arrow, so it can't be mistaken for Previous beside it.
- **The same controls everywhere:** the mini-player, the floating window and the banners on Live TV and Radio show the same buttons in the same order as Now Playing. Where they don't fit on one line they wrap onto two, so none is left out. On a narrow Now Playing page the volume slider gives way first and the mute button stays.
- **Multi-View:** each stream's close button is the same as the player's, and hides when the pointer rests.

### Fixes

- **Skip messages behind Up Next:** "+10s" or "Speed 1.5×" could be hidden behind the Up Next card. They now appear near the top of the picture.
- **Up Next over a dropped connection:** Up Next and Skip Intro could cover the message that a stream had dropped. They now step aside until it's back.

## v0.28.02: Opens Again (29 October 2026)

ElBee Player no longer depends on a developer certificate, so it can't stop opening when one is withdrawn. If ElBee Player won't open, please download this version manually from elbeehq.com or GitHub.

### Fixes

- **Opens again:** earlier versions were signed with a developer certificate that Apple has since withdrawn, which stops them from opening. This version is signed without one, so that can't happen again. If ElBee Player won't open, please download this version manually from [elbeehq.com](https://elbeehq.com) or [GitHub](https://github.com/ElBeeHQ/ElBeePlayer/releases/latest), open the disk image and drag ElBee Player onto Applications, replacing the old copy. Your playlists, favourites and settings are kept.
- **The first time you open it:** macOS may say it can't verify the app (open **System Settings › Privacy & Security** and click **Open Anyway**), and may ask once whether ElBee Player can use the sign-in details it saved: click **Always Allow**.

## v0.28.01: Catch-Up and a Clearer Player (29 October 2026)

Watch programmes that have already aired from the new Catch-Up tab, rewind live TV from its timeline, and use a cleaner, redesigned control bar.

### New

- **Catch-Up:** a new **Catch-Up** tab, shown when your playlist has channels that keep an archive, for programmes that have already aired. Browse **Just Finished** and a shelf for each channel, or pick a channel in the sidebar, where they're grouped under the same categories as Live TV and follow your **Content Languages** and hidden categories. Point at a programme and move along it to choose where to start. It works with M3U playlists that carry catch-up details too.
- **Catch-Up Preview Frames:** pointing at a programme can show still frames from the archive as you move along it. **Settings › TV Guide › Catch-Up** sets whether they load always, only when nothing is playing (so they never interrupt what you're watching on a one-connection plan), or never.

### While you watch

- **Redesigned player controls:** Now Playing and full screen share one cleaner control bar. The programme or elapsed time sits at the top with the time left at the right, the timeline runs the full width beneath them, and the controls below are in three zones: **Record** (now a labelled button) and Favourite on the left, Play/Pause in the exact centre with the same number of controls either side, and Subtitles, Cast, the volume, **More** and Full Screen on the right. **More** gathers the playback options, the video settings and Float Video. Every button lights up under the pointer and its tooltip says what it does and which key does the same. The icons share one outline style and size, the speaker's waves follow the volume, and the Up Next card lines up with the bar.
- **Rewind live TV:** on a channel that keeps a catch-up archive, the live timeline is now a seek bar. Click or drag back along the programme to watch from there (to the minute), or use **Rewind 1 Minute**, and **Jump to Live** takes you back. On a channel without an archive the timeline is a plain progress line, and its tooltip says the channel can't be rewound.
- **Seek bar:** pointing at it thickens the track, grows the handle and shows where a click would land: a lighter fill from the current position to the pointer and the time there ("1:23 / 4:56"). With keyboard navigation on, Tab reaches the seek bar and the volume slider: on the seek bar the arrow keys move 5 seconds (a minute in the archive), and Home and End go to the start or end. VoiceOver reads the position as "1 minute 23 seconds of 4 minutes 56 seconds".
- **Easier to read:** the LIVE badge is a deeper red so its text stands out, the slider tracks are clearer against the glass, and with keyboard navigation every player button shows which one has focus.
- **Speed and sleep timer at a glance:** while a movie plays at another speed, or a sleep timer is set, a small chip beside the other controls on the right shows it ("1.5×", "25 min"). Click it to go back to normal speed or turn the timer off.
- **Scroll for volume:** scroll up or down over the picture on Now Playing or in full screen to change the volume, with a small meter showing the level.
- **Connection status:** when a stream drops, the picture says so wherever it's showing (full screen, Now Playing, the mini-player, the floating window and banners): **Reconnecting** with each attempt, **Waiting for the network** while your Mac is offline, and **Connection Lost** with **Try Again** if it can't come back.
- **Seeking in the archive:** in Catch-Up and **Start from Beginning**, the seek bar shows the programme's own time and you can move anywhere in it. The skip buttons and the ← and → keys move a whole minute there, the smallest step an archive allows. Skipping past what has aired in Start from Beginning takes you back to the live channel.

### Improved

- **Live captions:** a darker plate and brighter text, so captions stay readable over a bright picture, with words still being worked out easier to make out in Light Mode.
- **Sidebar headings:** folded country and category headings are easier to read in Dark Mode.

### Fixes

- **Mini-player:** no longer disappears on the Catch-Up page after you leave Now Playing.
- **What's New:** the toolbar buttons no longer show over the What's New panel.

## v0.27.01: Start from Beginning and Skip Intro (28 October 2026)

Watch the programme on now from its start, and skip a series' opening titles with one click.

### New

- **Start from Beginning:** on a channel that keeps a catch-up archive, watch the programme on now from its start. It's in the player's controls and in the Live TV and TV Guide banners. **Go Live** takes you back to the channel, and you return to it by yourself when you catch up.
- **Skip Intro (Beta):** ElBee Player learns each series' opening titles by comparing the start of one episode with the next. From then on, **Skip Intro** appears over the picture while they play. **Settings › Playback › Player** can turn it off, have it skip by itself, or forget what it has learnt.

## v0.26.02: Clearer sign-in wording (27 October 2026)

Accounts you sign in to with a server address, username and password are now called Server Sign-In.

### Improved

- **Server Sign-In:** the sign-in screen and **Manage Playlists › Add Playlist** call this kind of account **Server Sign-In**, beside **M3U Playlist**. Your saved playlists, favourites and history are unchanged.
- **Clearer message:** when a server sends something the app can't read, the message now asks you to check it's the server address your service gives you for signing in with an IPTV player.

## v0.26.01: M3U playlists (27 October 2026)

M3U playlists join server sign-in accounts, Manage Playlists is redesigned with backup addresses for each account, and ElBee Player now installs from a disk image.

### New

- **M3U playlists:** add a playlist from a web address or a file on your Mac, alongside accounts you sign in to with a server address, username and password (**Manage Playlists › Add Playlist**, or the sign-in screen). Its TV guide comes from the address the playlist names, or one you enter.
- **Backup addresses:** give an account other addresses for the same service. They're tried in order when the main server doesn't answer, each shows whether it's working, and the playlist list warns when one stops responding.
- **Install window:** ElBee Player now downloads as a disk image. Opening it shows the app beside your Applications folder, ready to drag across. Copies already installed keep updating from inside the app as before.

### Improved

- **Manage Playlists:** redesigned, with every playlist in a sidebar showing its status and library size, a larger **Add Playlist** button, tidier details, and nothing to scroll past to save. Drag playlists to reorder them; editing a playlist's server or username keeps its favourites and history.

### Fixes

- **Banners:** a faint dark line no longer runs half way across the banner on Home, Live TV and the TV Guide, and the picture's glow now spreads smoothly behind the text.

## v0.25.02: elbeehq.com (27 October 2026)

ElBee Player has a website: elbeehq.com, with downloads, the notes for every release, an install guide and support.

### New

- **elbeehq.com:** download the latest version, read What's New for every release, and find an install guide, answers to common questions, keyboard shortcuts and a way to contact us.
- **Linked from the app:** the website sits at the foot of the sign-in, playlist chooser and loading screens, in **About ElBee Player**, in **Settings › About** and at the bottom of the **What's New** panel. The update window links to it under the notes.
- **Help menu:** **ElBee Player Website**, **Release Notes** and **Report a Problem**, in place of a Help item that had nothing to open.
- **Settings › About:** a **Website** row, **Legal & Terms** beside the licence, and **Report a Problem** under **Support**.

## v0.25.01: Playback options, Pin to Home, What's New (26 October 2026)

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

## v0.24.02: Sharpening, subscription reminder, download progress, lighter Live TV and Guide (26 October 2026)

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

## v0.24.01: Smooth Picture Moves by default, HDR, stream colours, subtitles on hardware (26 October 2026)

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

## v0.23.02: Subtitle timing, a clearer Subtitles button, less work while playing (26 October 2026)

Subtitles you can line up with the dialogue, a clearer Subtitles button, and less work while you watch.

### Subtitles

- **Subtitle timing:** when a channel's subtitles run ahead of the dialogue or behind it, move them with **Show Earlier** and **Show Later** in the player's Subtitles button, or **View › Subtitles Earlier (⌘[)** and **Subtitles Later (⌘])**, in half-second steps. The timing is remembered for each channel, film and episode, and **Reset Timing** puts it back.
- **A clearer Subtitles button:** it's split into **Subtitles from the Channel** (Show Subtitles, Language and Timing) and **Live Captions · Made on This Mac**, so it's clear where each comes from. Language and Timing are now submenus, so the menu stays short however many languages a channel has.
- **One at a time:** turning on subtitles turns Live Captions off, and the other way round, so two lines of text never sit over the picture. Subtitles on by default no longer switch on over captions you've turned on.
- **One Text Size:** a single Text Size sets the size of whichever is showing. Subtitles a channel sends as pictures (most live TV subtitles) keep the channel's own size, and the menu says so rather than offering a size that can't change them.
- **4K subtitles with Smooth Picture Moves:** a 4K or 10-bit film stays on hardware decoding with subtitles on, rather than taking several processor cores. Its subtitles can't show with Smooth Picture Moves, and the Subtitles button says to turn it off for them.

### Lighter on your Mac

- **Less work while playing:** the player no longer refreshes its controls, the glow, the Now Playing info and the frame-rate check several times a second for nothing. They update when something actually changes, such as the picture's size or frame rate becoming known.

## v0.23.01: Casting, a playlist chooser at launch, and far lower energy use (26 October 2026)

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

## v0.22.01: Searchable Settings, new settings and shared player controls (25 October 2026)

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

## v0.21.02: Roll-up Live Captions (25 October 2026)

Live Captions that are easier to follow.

### Player

- **Live Captions roll up, two lines at a time:** words appear one after another at the end of the bottom line, and when it's full the line moves up and a new one starts below. Words you've already read stay where they are instead of shuffling along with every new word, and the plate keeps one size. Words the Mac is still working out are a little dimmer and settle once it's sure of them. Speech carries straight on from one phrase to the next, and the captions clear after a few seconds of quiet.

## v0.21.01: In-place full screen, Live Captions and banner glow (25 October 2026)

Full screen in one smooth move, Live Captions, and the picture's glow behind the banners.

### Player

- **Full screen in one smooth move:** the picture grows from where it is to fill the screen, and shrinks back to Now Playing, with no slide to a new Space. The menu bar and Dock hide while you watch and come back when you point at them. If you'd rather have full screen in a Space of its own, to swipe between it and your other apps, turn on Settings › Playback › Display › Use Full-Screen Spaces.
- **Live Captions (experimental, macOS 26):** your Mac can write captions for live channels that have no subtitles of their own, from the channel's sound, on your Mac. Turn them on in Settings › Playback › Subtitles & Audio (after a restart), then from the Subtitles button.

### Polish

- **Ambient Glow behind the banners:** the Live TV, Guide and movie banners take on the picture's light, and the mini player's glow spills out across the page beside it.
- **One click** on a banner's picture opens Now Playing.

## v0.20.01: Movie banner, live Subtitle Size, quiet launch resume (25 October 2026)

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

## v0.19.01: Plain Look and Smooth Picture Moves (24 October 2026)

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

## v0.18.01: Uniform player controls, glass close cross, hover controls on the live preview, and a rebuilt picture glide (24 October 2026)

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

## v0.17.01: Live TV, TV Guide and Radio redesigns, live preview, and first-time setup (23 October 2026)

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

## v0.16.01: Advanced Video, ambient light, Now Playing for movies and episodes, and system glass (23 October 2026)

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

## v0.15.01: Home screen, Content Languages and reorganised Settings (23 October 2026)

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

## v0.14.01: Section tabs, faster TV Guide, Interface Size and reset options (23 October 2026)

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

## v0.13.01: Richer detail pages, Light Canvas icon and migration clean-up (22 October 2026)

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

## v0.12.01: Amber theme and Prism app icon (22 October 2026)

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

## v0.11.02: Updating fixes for copies installed under the previous name (22 October 2026)

Fixes updating to ElBee Player from inside the app. There are no other changes.

### Updating

- **Copies installed under the old name can now update.** The in-app updater could not install version 0.11.01 on a copy
  still called LiquidIPTV, and reported the update as improperly signed. That message was misleading: the updater picks the
  app to install by the installed app's file name, and the rename had changed it. Updates for those copies now carry the app
  under the name they expect. Your data comes across as described for 0.11.01.
- **The app may keep its old file name** in your Applications folder after updating (it still says ElBee Player inside).
  You can rename it to ElBee Player in Finder at any time. Later updates work either way.
- Version 0.11.01 can still be downloaded and installed by hand; it simply could not be installed by the updater.

## v0.11.01: A new name: ElBee Player (22 October 2026)

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
- The description of supported services is clearer.

## v0.10.02 (22 October 2026)

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

## v0.10.01 (22 October 2026)

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

## v0.9.91 (22 October 2026)

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

## v0.9.82 (22 October 2026)

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

## v0.9.81 (22 October 2026)

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
