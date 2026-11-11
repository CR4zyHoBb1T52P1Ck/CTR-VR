# CTR VR v0.3.0 - Theatre and Creator Studio

A milestone update for filming, Photo, controller-friendly menus and content
creation. The owner accepted the final REC editor and preceding Theatre/Photo
candidate. The Windows package retains that exact tested game executable.
Earlier releases and local working installations remain available for rollback.

## Start here

1. Extract the complete Windows ZIP into a **new writable folder**. Keep your old
   installation. Open **CTR VR Launcher.exe** and supply your own compatible raw
   NTSC-U disc BIN. No retail data, personal saves, settings or device keys are included.
2. Choose **Play in VR** for Windows SteamVR/PC streaming, or **Flatscreen** for
   headset-free keyboard/gamepad and calibrated-wheel play. Keep a complete package;
   do not replace only the game EXE in an old installation.
3. For VR, set the headset refresh in SteamVR **before launching**, then use the
   launcher's maintained Native timing profile. **90 Hz is the reference/default**.
   Developer headset testing covers **80, 90 and 120 Hz**; use 80/90 when more
   headroom is needed and 120 when your system sustains the heavier workload.
   Restart after changing headset Hz so the game and headset timing agree.
   **144 Hz remains EXPERIMENTAL**. These are supported test paths, not an all-track
   full-speed guarantee. Heavy races and Creator/OBS workloads can still slow down.
4. In game, pause and open **F9 Settings** (or the mapped controller settings
   shortcut). Home links to **Photo** and **Theatre / race takes**. Point/trigger or
   touch the interactive panels; stick/D-pad/keyboard navigation remains available.
   Grip a panel's title to move/tilt it; grip + stick changes size where labelled.
   Hover explanations distinguish Photo PNGs, Theatre takes and Creator/OBS video.

## Theatre: record a race, then direct it

- After GO in a loaded race, pause > F9 > **Theatre > Record take on resume**.
  Resume with the controller. Red REC/timer confirms recording. Pausing seals the
  take; **wait for SAVED**. F7 is an optional keyboard start/stop. Alt+F11 saves a
  frozen scene. Photo, tracking loss, scene/mode changes and safety limits can end
  a take. Quit normally before opening it in the launcher Theatre library.
- Choose **Desktop director** or **Tracked VR viewfinder**, select a completed
  scene/take, then **Open selected capture**. Double-click uses the same selection.
  The tracked viewer uses **PC SteamVR**, including Frame PC streaming; it is a
  gold viewfinder in a VR room, not immersive surrounding course geometry.
- Free camera or player anchor; move, aim, zoom and roll. In tracked VR use head-
  directed filming or grab the handheld camera. Tools can be moved separately by
  gripping their title. Pointer buttons, timeline dragging and hover help are usable
  alongside keyboard/gamepad commands; held grips do not globally disable commands.
- Play/pause, reverse, frame stepping, second/ten-second seeks, playback speed,
  In/Out ranges, looping, **64 bookmarks** and **eight saved camera shots**.
  D-pad **Up/Down changes camera speed**, **Left/Right scrubs** with Tools closed;
  inside Tools it selects buttons. A records/stops, X plays/pauses, B pauses with
  Tools closed; A confirms and B backs out inside Tools. Keyboard F10 records;
  T / gamepad View hides the editor. The in-launcher **Controls guide** lists the
  full keyboard, gamepad and tracked Frame mappings, including rise/fall controls.
- Export a clean silent H.264 MP4, **1280x720 landscape or 720x1280 portrait**,
  up to **30 minutes** within the resource limits. Select In/Out to export clips
  from different camera angles. The editor rails, gold border and laser are omitted.
  **30 fps is a workload-dependent target**, not a promise of 30 distinct frames.
  Clips: **Videos/CTR-VR/Replay Clips**; projects/bookmarks: **Director Projects**.

These are observed draw/texture takes, not deterministic game-state replays.
Off-camera geometry, objects and effects that were never retained may be missing.
Audio, genuine animated frozen holds and full immersive Theatre remain unfinished.
A frozen scene has no moving timeline. Unfinished .partial captures are kept out
of the completed library. Keep originals; archive/project files are not video.

## Photo, freecam and the loaded kart viewer

- Pause in a loaded hub/course and select Photo. The mode prepares a bounded frozen
  scene and textures, with orbit/free camera, head-relative movement, lock/head
  follow, exact gold-framed PNG preview, world drag/two-hand scale and visibility
  groups. The loaded kart/driver viewer reuses these tools. Unsupported states such
  as transitions can refuse capture instead of using unsafe scene data.
- New interactive Photo/Viewer tools sit beside the image, with buttons, hover
  explanations and optional controller hover haptics. Grip the title to place/tilt;
  grip + stick sizes it. **F1 / Frame right X / gamepad Start** focuses or hides tools.
  In focus, either stick/arrows selects, A/Enter activates and B/Esc hides tools first.
  Outside focus B/Esc exits Photo, keeping the game paused. World grabs remain
  available away from the tools title. Photo return preserves normal input handoffs.
- **Frame Photo:** right trigger PNG, right A orbit/free, right B return, right Y
  reset; **left bumper lowers / right bumper raises**. **D-pad Left/Right selects
  filters; Down/Up changes opacity**. Gamepad X saves, Y resets and LB/RB lowers/
  raises. In Orbit these height controls change elevation. Index filter thumbpads
  retain their vertical mappings; controller legends show the active hardware.
- Keyboard Space/F12 PNG; [ / ] previous/next look; comma/period opacity; O Original;
  Shift+V wide/portrait. P frame/stereo, L lock/follow, Q/E height, Page Up/Down
  distance. H shows hardware help. The complete guide lists movement and lens controls.
- Ten looks: **Original, Vibrant, Warm Postcard, Cool Dusk, Black & White, Sepia,
  Noir, Soft Pastel, Night Vision and Neon Arcade**. Opacity blends with Original;
  Original/0% bypasses grading. Existing preset IDs are preserved. New looks use the
  existing deterministic colour pass; they do not add another scene render.
  Looks apply to Photo/Viewer previews and PNGs, not live race video or Theatre MP4s.
- Photo PNGs support wide/phone portrait at the existing quality presets. The
  image inside the gold frame is the composition reference; panels/help are omitted.
  Save location: **game/Captures** in the installation used. Wait for PNG completion
  before changing aspect. Viewer animation for supported loaded models remains
  experimental; a complete 3D Garage/roster selector is not being claimed.

## Creator Capture and OBS

Enable the launcher's Creator capture window, choose the view, framing, quality,
rate and overlays, then save settings. **Record the window titled CTR VR Capture**
in OBS. The game/SteamVR mirror remains the headset view; Chase only changes the
separate recording output. OBS recording and Theatre takes are different systems.

Eye Fill/Fit reuse a headset eye. Clean Mono, Stabilized Forward and Chase offer
recording-specific cameras; **Chase/Stabilized remain experimental views**. Chase
has optional first-person PiP, large/small view swap, all corner snaps, free position,
size and Classic or thin **Gold full-image frame**. PiP reuses the available images.
Wide/phone portrait works across Creator views and Photo; Theatre has its own
independent aspect selector. Eye Fill crops and Eye Fit can show bars.

In F9 > **Creator / Capture > Recording Layout / PiP**, adjust output/framing and
**Show settings menu in OBS**. The paused custom menu and explanations can appear
in recordings; the REC placement editor uses the completed eye so its lasers/badge
are visible too. Photo and Theatre clean exports continue to exclude editor UI.
Recording HUD/status controls affect separate mono/Chase overlays; they cannot
remove HUD already baked into an eye/PiP image. HUD Layout Visibility hides the
currently selected headset widgets without discarding their individual choices.

**Primary preview Off / black** disables the optional desktop headset mirror while
keeping Creator output active. Keep the main game window open/focused for inputs.
This differs from OBS's own preview toggle. Extra capture and OBS work still cost
CPU/GPU time. Eye Fill/Fit are the lower-cost fallback; no full-speed recording
or arbitrary minimized Window Capture guarantee is made.

## Menus, REC placement and retained controls

- Interactive mod settings pages, clear hover explanations, cyan targeting, gold
  selection, optional short hover haptics, controller proximity touch, desktop
  mouse input on a visible main mirror, and grabbable titles. Dedicated calibration
  and raw remapping keep their guarded input ownership. Both sticks/D-pad and
  keyboard paths remain available where labelled.
- **HUD / Layout > REC indicator placement > Grab REC badge / frozen preview**:
  point a cyan laser, hold grip or trigger to move/tilt, stick Up/Down to size,
  then **Done / Save**. B cancels the draft. **Kart is the default anchor**; Head and
  World are optional, with saved choices respected. Placement is frozen while
  editing, so looking around does not move the target. This badge indicates take
  recording, not OBS, and changing it does not arm or stop the recorder.
- Retained Index/Frame motion control paths, thumbstick, hand-position and virtual-
  wheel steering, calibration/remaps, first/third-person cameras, comfort settings,
  original-art HUD and modular widget placement. Gamepad/keyboard and calibrated
  wheels remain available, including headset-free desktop play. Directional D-pad
  throws and mixed wheel/motion gesture attacks retain their saved options.
- Optional physical-wheel force feedback and progressive pedal mode remain
  **experimental and OFF by default**. Conservative FFB defaults remain; broad
  hardware/feel acceptance is not established. Steering-wheel acceptance is
  deferred while the maintainer's wheel is packed away.

## Compatibility and honest limits

- **Windows PC VR:** developer use covers Index and Frame PC streaming; 80/90/120 Hz
  paths have developer testing. Not every control/hardware combination is certified.
- **Quest 3:** community PC/SteamVR compatibility reports, distinct from developer
  hardware testing. This is not a Quest standalone build.
- **Steam Frame local flatscreen:** the maintainer's preserved Non-Steam/Proton
  installation has owner acceptance and stays separate from experimental VR. This
  Windows ZIP does not install it onto a headset; a portable clean-user installer
  is not included. PC-streamed and local standalone play are different modes.
- **Steam Frame standalone VR:** boots/races in private tests but remains too slow
  for supported play. Experimental, no locked 80/90 Hz or native ARM port claim.
- **144 Hz:** experimental. Heavy tracks, nearby racers and Creator/OBS can still
  cause timing dips. Buffer reuse, state/query/capture refinements and diagnostics
  improve code paths; they do not establish that all slowdowns are solved.
- Custom tracks/recovered courses and test-map directors have private prototypes,
  but full custom eight-racer gameplay, universal XDELTA compatibility, multiplayer,
  complete Garage, flat motion/Photo parity and DLSS remain roadmap work.

## Preserve, verify and build

Back up the old installation with the game closed. Keep the new binaries,
bindings, manifests and defaults together; move personal settings/cards selectively.
Never upload a private test package containing disc paths, saves or session data.
Use the named Windows and **complete source ZIPs** plus SHA256SUMS.txt. GitHub's
automatic source archives contain only the public documentation repository.

The corresponding source ZIP contains the patched native tree, VR bridge,
launcher/tooling, pinned OpenVR and vendored SDL. Run its **Build-Source.ps1** using
Visual Studio 2022/2026, CMake and the .NET compiler; no disc or headset is needed
for compilation/CPU tests. Byte-for-byte reproducibility is not claimed. The
published Windows game hash pins the exact owner-accepted executable.
Read **BUILD-SOURCE.md**, **Theatre-Controls.md**, **Steam-Frame.md** and the included
credits/full license texts. The native integration is GPL-3.0-or-later; launcher/
standalone tooling has MIT terms; third-party assets retain their notices.

Feedback exports an allowlisted summary for review and deliberately opens an
issue draft. There is no automatic log/video upload, token storage or untrusted
report-to-code automation. Thank you to the owner, community testers and creators
helping shape this unofficial project.
