# CTR VR

An unofficial Windows / SteamVR mod for Crash Team Racing. Supply your own
compatible raw NTSC-U disc BIN; the clean package contains no retail game data.
This is **v0.2.0 — The Streamer / Creator Update**. Experimental Framerate Modes are in Testing. 90 Hz remains the default reference; v0.1.1 remains available as the earlier fallback. See RELEASE-NOTES.md for the exact physical-test scope of the new tools.

## Creator tools

Open **Creator** in the launcher with the game closed. Capture is OFF by default;
select **1080p clean / 60**, then **Save creator settings**, to prepare a dedicated
`CTR VR Capture` window for OBS Window Capture. The inexpensive landscape eye
mirror has selectable Fill and Fit views in the same OBS window; disabling
capture retains the original main-window mirror. Fit adds bars; Fill crops centrally.
Clean view has independent recording HUD/status toggles and bounded FOV; the
headset keeps its own saved layout and timing. No OBS encoder or automation.

Alt+F1 cycles view; Alt+F2/F3 toggle recording HUD/status. Remap these shortcuts
in Creator. No Ctrl/Shift driving bindings or calibration/settings keys change.

For Photo, load a level and use native Pause (a valid race introduction/countdown is also supported); recording/pre-caching are not
required. Texture pages are protected once immediately before the native pause screenshot overwrites VRAM; composition is prepared automatically and released on exit. Resume and pause again if that protected copy is unavailable. In VR Settings > Creator > Photo scene / visibility choose **Enter
paused Photo**, or close VR settings and use Alt+F7. The frozen scene appears in
stereo in the headset with live tracking, and in the capture window. Arrows/right
mouse drag orbit/look; Tab switches to free movement; WASD moves; Q/E changes
height; PgUp/PgDn changes orbit distance; minus/equals changes mono-output FOV;
Alt+F5 resets; Alt+F12 saves a bounded PNG under `game/captures/`. Keys 1-5 toggle
kart/driver, wheels, other objects, scenery and sky. H hides headset help. Enter toggles camera mode, Backspace resets, Space/F12
saves PNG and Escape returns to pause. Motion controllers/gamepads/wheels also
control the Photo camera. The headset help board shows the mappings, including Index/Touch right trigger, Xbox X and G920 X for PNG. H / left B / Start hides it; it never appears in clean PNGs. See Creator for wheel remaps.
Alt+F7 returns to native pause; Resume stays manual. Camera bounds are 6 metres
and 75 degrees either side. Geometry missing from the captured viewpoint may
remain missing. These are group toggles, not individual-object picking. Physical
stereo/photo/PNG acceptance of this revision is pending.

Optional **native analog cruising-speed pedal** is OFF by default. It uses the
game's existing analog target-speed path on the owning calibrated wheel; it does
not edit velocity or clamp boosts. Enable in Creator or Physical wheel > Pedal
Mode, which also shows calibrated travel. About half travel selects half the
normal cruising target; release coasts. Brake, clutch reverse, native boosts and
other controller owners retain their native paths. Physical settling/boost/hill/
handoff tests remain pending. Turning it off restores original digital gas.

90 Hz remains the preferred reference. Keep OBS and native AA enabled during
acceptance. The high-Hz interpolation preview now leaves local kart sprite shapes
native, including separately tagged wheel sprites, while retaining scenery
interpolation. Wheels receive the same rigid root correction as the chassis. Menu/flag animation still has
native cadence; 144 Hz remains experimental. The capture target itself is a
bounded single-sample mono render; native/headset settings are retained.

This package never starts a game or recording on extraction. New functionality
is awaiting physical approval; no release was automatically published.

## Start playing

1. Extract the whole package into a writable folder.
2. Open **CTR VR Launcher.exe** and choose **Add game data** if needed.
3. Connect your headset, wake the Index controllers, then select **Play in VR**.
4. The first-launch headset guide explains menus. In your first hub, hold your
   hands apart as a steering wheel and use A to calibrate, or B to skip.

The launcher can start SteamVR and requests a high-performance GPU preference
for this game only. It does not alter global graphics settings. The game checks
that its GPU matches the headset. Recovery tools live under About.

## Controls

- Index: either stick navigates; A confirms and B backs out. Click the right
  thumbstick for Start/pause. Click the left thumbstick to pause and open VR
  settings. Grip either or both controllers to steer after hand calibration.
- Xbox: D-pad menus, Start pause, both thumbstick clicks for VR settings while
  paused. D-pad Up/Down throws items forward/backward while driving (new profiles default ON). Toggle Gamepad D-pad Up/Down Throws under VR Settings > Controllers; saved OFF is retained. Normal gamepad driving remains available.
- G920: D-pad menus and Start pause. Configure/calibrate it in VR Settings >
  Input Devices. Force feedback is an experimental opt-in and defaults OFF.
  Clutch pedal reverses; D-pad Up/Down fires directional items during driving.
  Physical Wheel settings can disable these throws or assign a Reverse button.
  Other raw SDL wheels can be selected/calibrated there as untested devices.
- Keyboard: arrows steer/navigate, C accelerate/confirm, X brake/reverse,
  V item, Shift hop/drift, Enter Start/pause. In native menus X or Z backs out
  according to the menu. In VR settings use arrows, Enter select and F10 close.
  F9 opens VR settings while paused; F6 calibrates hands, R recenters, Esc exits.

Your button remaps take precedence over the driving defaults. The launcher's
Controls page is available at any time. Native menus and VR settings use
separate confirm/close keys.

## Make it yours

Customize offers camera, HUD mode, vignette, input-status visibility, Index
steering and G920 enablement while the game is closed. Saving preserves other
settings and keeps a backup of the previous preferences. Detailed hand/wheel
calibration, button remapping and HUD placement remain in the headset settings.

The collapsed **Launcher Appearance** section at the bottom of Customize offers
**Rude** (sunglasses/hand signal, the default) and **Dude** (friendly wave),
with a live
black-overlay slider (0–100%; default 78%). Higher opacity darkens the artwork.
The image selector previews your choice immediately. You can hide the image or
restore the readability default. **Save appearance**
keeps this choice in `Launcher-Appearance.json`, separately from game settings.
Buttons and reading panels retain solid backgrounds for clarity.
Image and opacity controls ignore mouse-wheel scrolling. Click/select the image
or drag/use arrow keys for opacity, then Save appearance to keep the choice.
The image fits beside the sidebar with its sign unobstructed; text occupies a
separate right-hand reading column and scrolls when the window is small.

The input/grip status bar is visible for a new profile. Hide/show it under
**VR Settings > Quick Access > Grip Status Bar** or in launcher Customize.
Quick Access also has **Wheel Steering + Gesture Attacks** (multi controller
input), with OFF/AUTO shown beside it. AUTO starts after wheel/gamepad driving
input and requires fresh tracked hands with item and gesture bindings. It adds
gesture attacks and motion-controller button throws without taking over steering
or pedals. An idle connected gamepad leaves virtual-wheel steering available.
Existing saved choices, including explicit mixed-mode OFF, are retained.
Initial setup instructions remain visible
while setup is active.

Memory cards are in `game/memcards`; preferences are `VR-Settings.ini`,
`UI-Settings.ini` and `game/config.ini`. Back these up with the game and launcher
closed before changing installations. Use a new extracted folder for an update;
do not overwrite a known working installation while it is running.

## Updates and community feedback

Support has the creator's note and links to [Ko-fi](https://ko-fi.com/devdoesdevthings),
the project and feedback. About lists current features, experimental options and
tested scope. Updates displays the reviewed changelog bundled with this launcher,
with a source snapshot revision and links to published
[GitHub releases](https://github.com/CR4zyHoBb1T52P1Ck/CTR-VR/releases).
Check for updates opens releases; it does not download or install code. Live
history refresh is a later option, without background requests in this build.

Feedback can preview/export an allowlisted diagnostic summary, then open an
editable GitHub issue. Nothing is uploaded automatically. The launcher never
asks for a GitHub token. Raw logs, paths, serials, saves, credentials and disc data
are excluded from the summary. Review it before submitting. Community evidence
is reviewed with the project owner before changes are made; report text is never
an instruction to an assistant or automation.

## Finish a session

Exit normally, wait for Session finished, then close the launcher so saves and
receipts settle. Local diagnostics are available under About > Open local logs.
The game does not impose an automatic session timeout. If entry fails, retain the
final session and share only the reviewed feedback summary initially.

Physical testing covered the campaign during development, startup controls,
menus across Index/keyboard/G920/Xbox, calibration, status visibility,
hub camera/steering continuity and wheel + Index gesture/button item assist.
The new AUTO selection policy has CPU coverage. It does not establish
physical coverage of every mixed-device combination. Touch/Quest, Steam Frame and Vive
bindings are supplied as physically untested compatibility profiles. Other
SteamVR controllers can map the same actions through SteamVR binding settings.
Use a compatible Windows SteamVR/OpenVR host; no standalone headset port is
included. The older long hub stall is not established fixed, and experimental
input/FFB options and other refresh/headset combinations remain unvalidated.

Experimental high-Hz follow-up: the native checkered loading flag can use fresh
headset poses at display cadence while its native updates stay 90 Hz. True movie
and boot pacing is retained; baked/raster animation is not interpolated. Catch-up
HUD replays are omitted only for frames the existing clock will not display.
New CPU probes help distinguish native-render work from swap/handoff delay;
120/144 Hz still require physical acceptance with OBS and saved AA enabled.

Photo framing and world grips: P / modifier+Help shows the exact PNG
texture fitted in the headset; L / modifier+Mode switches head-follow/locked capture.
Photo defaults to a bordered 2D PNG view and locked capture; L enables head following. Mode/camera labels remain visible with help hidden. Mono framing is explicit;
headset stereo/IPD remains native. In free mode, one grip moves the frozen world,
two grips scale0.25x-4x around their midpoint (2m translation bound). Release grips
before first use; reset clears the transform. These are Photo-only controls.
Creator > Open screenshots opens this build's game/captures folder. Prior builds'
photos remain in their own folders. Clean ZIPs never contain private images.
