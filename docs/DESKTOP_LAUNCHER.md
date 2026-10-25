# CTR VR

An unofficial Windows / SteamVR mod for Crash Team Racing. Supply your own
compatible raw NTSC-U disc BIN; the clean package contains no retail game data.
This is the v0.1.0 player release.

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
  paused. Normal gamepad driving remains available.
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
