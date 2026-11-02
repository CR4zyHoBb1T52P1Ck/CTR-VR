# CTR VR v0.2.5 — player and Creator guide

Unofficial Windows native/SteamVR mod. Supply your own compatible raw NTSC-U disc
BIN. Read RELEASE-NOTES.md for the full change list and limits. **90 Hz remains the
reference;144 Hz is experimental.**

## Start, update and preserve

1. Extract the entire Windows ZIP into a new writable folder; verify SHA256SUMS.txt.
2. Open **CTR VR Launcher.exe**, add your disc and choose **Play in VR** or
   **Flatscreen**. Flat play supports native keyboard/gamepad and calibrated wheels
   without a headset. VR Photo/overlays/motion input are not flat features yet.
3. For VR, connect the headset/controllers and set actual Hz before launch. Movies,
   menus, loading and results intentionally use a tracked panel; assess stereo
   in a playable single-player hub/race.
4. Preserve the complete old installation. With game/launcher closed, back up and
   selectively transfer your own VR-Settings.ini, UI-Settings.ini, optional flat
   wheel/appearance settings and game/memcards. Keep the new runtime/bindings/
   manifests/defaults/config together. Screenshots remain in their original
   installation's game/Captures folder. Use the complete old folder as rollback.

## Headset refresh

Customize > Headset timing > **Save launch settings**. Set80/90/120 on the headset
first, then select Current Native;90 reference also requires a 90 Hz headset.
120 is developer-tested with OBS and AA, but heavy races/Creator can still slow.
144 is experimental;72 is physically untested. Experimental clock recovery and
legacy interpolation are separate comparison profiles, not guaranteed full-rate
rendering. Restart after a Hz change. The in-game FPS picker does not change
headset refresh; effective rate matching preserves saved FPS/calibration.
Keep Native 3D and native game Mirror mode off. See FRAME_RATE_GUIDE.md online.

## Controls and physical wheels

Index right stick click pauses; left stick click opens VR settings. Either stick
navigates native menus, A confirms and B returns. F9 opens settings from keyboard.
Thumbstick/hand-position/virtual-wheel steering, hand calibration (F6), remaps and
wheel+gesture item mixing retain their established paths. The Controls page and
in-mode help show hardware mappings. Xbox/gamepad and G920 navigation are retained.
Input Devices configures wheel calibration, sensitivity and mappings. Flat wheel
options are independent of the saved VR profile. D-pad directional throws, braking
and clutch/button reverse are separate settings; saved OFF remains OFF.

FFB and calibrated progressive pedals are optional/experimental and OFF by
default. Conservative FFB starts 10%, capped 25%; motor/feel acceptance across
hardware is pending. Digital throttle remains available and native boosts are
retained. Device changes require fresh calibration/mapping; do not reset a good
calibration while diagnosing timing.

## Creator Capture, PiP and HUD

1. Launcher > Creator: enable Capture window, choose recording view, preset,
   30/60 updates, FOV and recording HUD/status. **Save creator settings**.
2. For PiP choose **Use Chase + PiP**, the large view and one of four corners or
   Free position. Drag the diagram to move, its bottom-right handle to resize;
   arrows nudge and +/- resize when focused. Numeric X/Y/size controls are exact.
3. **PiP frame style** offers Classic 16:9 fit/bars or **Gold - full image, no bars**.
   Gold follows source aspect without cropping/stretching and bounds tall insets.
   The diagram is guidance; check actual output during gameplay.
4. Live VR changes: F9 > Creator / Capture > Recording Layout / PiP. Up/Down
   selects; A/Accept or Left/Right changes. Move / Resize PiP has placement/size
   rows and labelled grip interaction. PiP Style changes the border. Capture
   Reset is on the Creator parent page. Resume to see the recording layout.
5. OBS must capture **CTR VR Capture**, not the main game/SteamVR mirror. The
   headset stays in its gameplay view. PiP does not apply in Photo/menus/loading
   or eye fallback. Both large/small orientations remain available.

Eye Fill/Fit reuse an eye (Fill crops, Fit retains aspect with bars). Clean mono,
Stabilized and Chase add one world view at capture cadence. PiP reuses images;
swap adds copies/scratch storage, not another scene render. Eye Fill/Fit are the
inexpensive fallback. Chase has no collision avoidance and can use eye fallback
when pose/body/wheel geometry is unavailable.

**Recording HUD Hidden + Recording input status Hidden** removes main mono/Chase
overlays. Eye/PiP includes headset HUD. **HUD Layout Visibility** hides the current
selected headset layout without changing the individual widget choices.25 grouped
original-art widgets and saved placement remain.

**Primary desktop preview Off / black** reduces optional mirror copies/swaps while
CTR VR Capture remains live. Keep the main game window open for input focus.
OBS preview is a separate cost; minimizing/hiding the recording window itself is
not guaranteed safe for every OBS Window Capture setup. Match all settings for
comparisons; OBS and AA are not silently disabled by these optimizations.

## Photo, freecam, loaded model and looks

Load a level, pause, enter Photo through Creator's Photo scene/visibility menu or
Alt+F7 with VR settings closed. Scene/VRAM caching prepares/releases automatically.
The gold-bordered exact 2D preview is the PNG composition reference. P switches
preview; L changes locked/head-follow. Live tracking, orbit/free movement, FOV,
head-relative motion, one-grip drag, two-grip scale and group visibility remain.
Help around the viewfinder stays outside screenshots. Keyboard1–5 toggles scene
groups; Space or the displayed controller capture button requests a PNG.
Screenshots save to **game/Captures** in the current installation.

Index left thumbpad Up/Down adjusts opacity; right Up/Down selects next/previous
look. Keyboard [ / ] selects, comma/period adjusts strength, O restores Original.
Gamepad Photo D-pad Left/Right selects looks and Up/Down adjusts opacity;
thumbsticks move the camera. Original/0% bypasses effects. Photo preview/PNG
share the treatment. Controls are scoped to Photo and do not replace driving.

The loaded-kart viewer shares framing, visibility and screenshot controls;
supported models have experimental bounded current-clip playback (V play/pause,
N restart), otherwise frozen fallback. No roster browser or automatic stereo
garage/character-selection replacement is promised. Flat Photo/freecam is pending.

## Feedback, compatibility and limits

Feedback selects completed sessions by their recorded source/runtime identity.
Review the summary/optional OBS observations before exporting JSON or deliberately
opening an issue draft. No automatic upload, raw-log forwarding or credential
storage. Offline triage adds no per-frame text-processing worker. Include profile,
Hz, track/race, capture layout, OBS recording/preview and AA; distinguish music/
game slowdown from image judder. Missing context is not a zero or a pass.

Quest 3 PC/SteamVR compatibility has community reports relayed by the maintainer;
broader gesture/controller coverage, Quest 3S, Steam Frame and standalone ports
are not established. Developer headset tests cover80/90/120. Creator workloads
still need optimization. Custom tracks, multiplayer and theatre remain gated
work; no XDELTA source-check bypass or retail data is distributed.
