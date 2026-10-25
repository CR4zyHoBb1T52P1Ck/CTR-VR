# CTR VR v0.1.0 — grab the wheel

Bring Crash Team Racing into SteamVR with stereoscopic worlds, a first-person
kart view, a customizable original-art HUD and one- or two-handed virtual-wheel
steering. Play with Valve Index controllers, an Xbox gamepad, a Logitech G920 or
the keyboard, with a player launcher for setup, controls and customization.

This is the first full public release following the earlier alpha.
The mod is free, unofficial and unaffiliated with
the original game's owners, the Turbocharged team or Valve.

## What is included

- **Stereo worlds:** Adventure race tracks, five hubs and supported battle
  arenas, with animated textures, skies, actors and original game materials.
  Native startup, loading, results and supported cutscenes use a tracked screen
  where appropriate; true stereo character selection is future work.
- **Camera and comfort:** first- and third-person views, recentering, seating
  adjustments, comfort smoothing, optional vignette, local-body visibility and
  scripted-camera fallback.
- **Index driving:** thumbstick, hand-position or virtual-wheel steering;
  one/two-handed grip transfer, initial hand setup, recalibration, button
  remapping and directional item gestures. Native item restrictions still apply.
- **G920 and gamepad:** wheel/pedal calibration, button assignments, steering
  strength and source handoffs, alongside normal gamepad driving. Pedals trigger
  native digital driving actions; this does not replace the vehicle physics.
  A calibrated clutch pedal (or assignable wheel button) requests reverse.
  Wheel D-pad Up/Down fires directional items by default, with its own toggle.
  Other raw SDL wheels can be selected, calibrated and mapped as untested devices.
- **Personal HUD:** original artwork, text or hidden mode, 25 grouped widgets,
  saved hub/race and camera layouts, placement/scale/depth/yaw/tilt/visibility,
  paused placement tools and an optional grip/input status bar.
- **Player launcher:** disc import, permanent controls reference, first-launch
  headset guide, launch preferences, separate Support/About/Updates pages,
  adjustable rendered homage backdrop and reviewed release changelog. Update buttons open
  GitHub for manual review and download.
- **Untested controller profiles:** Touch/Quest, Steam Frame and Vive wand
  default SteamVR bindings. Other SteamVR controllers can map the same actions
  in SteamVR's binding UI. These are compatibility paths, not physical validation.
- **Optional feedback:** preview/export an allowlisted diagnostic summary and
  open an editable GitHub issue draft. There is no automatic upload or GitHub
  token. Raw logs, private paths, serials, saves and disc data are excluded.
  Community evidence is reviewed with the project owner before changes are made.

The campaign and bosses have been played through during development. Later
focused testing covered menus, calibration, controller handoffs and hub camera/
steering transitions. This is not certification of every mode or device.

## Requirements

- Windows with the .NET Framework 4.x runtime for the launcher, SteamVR and an
  OpenGL 3.3-capable graphics driver. The game is a 32-bit Windows build.
- The physically tested target is Windows 11 / Valve Index at **90 Hz**, with
  the supplied **90 FPS** configuration. Index, Xbox gamepad, G920 and keyboard
  paths are supported; other headsets, GPUs and refresh rates need more testing.
- Your own compatible **NTSC-U retail CTR raw MODE2/2352 BIN**. Renaming an ISO
  does not make it compatible. No retail disc data or personal saves are shipped.
- A writable extracted folder. Executables are unsigned. Keep the complete
  package together, including its manifest, DLLs, input files and licenses.

## Install and start

1. Download `ctr-vr-v0.1.0-windows-x86.zip` and `SHA256SUMS.txt`. Verify the ZIP's
   SHA-256 against the named entry; checksums detect changed files and are not a
   digital signature.
2. Extract into a **new writable folder**. Do not mix files from earlier builds.
3. Open **CTR VR Launcher.exe**, then **Add game data** to copy your own disc
   BIN. The original stays in place. Import can be canceled and does not replace
   existing game data. The game performs full compatibility validation at boot.
4. Connect the headset, set SteamVR to 90 Hz, wake the Index controllers if used,
   and select **Play in VR**. Keep the high-performance GPU request enabled;
   the game separately checks that its GPU matches the headset.
5. Read the first-launch headset controls guide. At the first playable hub,
   hold your tracked hands comfortably apart like a wheel, release grips and
   thumbpads, then press **A** to calibrate or **B** to skip. Release the button
   afterward. Recalibration is available in Quick Access.

Gamepad and keyboard driving remain available if you skip motion setup.

## Essential controls

| Device | Menus and pause | VR settings / driving |
| --- | --- | --- |
| Valve Index | Either stick navigates; A confirms, B backs out; right stick **click** is Start/pause. | Left stick **click** pauses and opens VR settings. Grip either/both controllers to steer after calibration. Default driving: right trigger gas, left trigger brake, A buttons hop/drift, right B item, left B rear view. Saved remaps take precedence. |
| Xbox | D-pad navigates; use native confirm/back; Start pauses. | Click both sticks while paused for VR settings. Normal gamepad driving remains available. |
| Physical wheel | D-pad menus; configured confirm/back and Start/pause. | Calibrate axes/assign buttons under VR Settings > Input Devices. Clutch pedal reverses; Up/Down fires directional items. Without a clutch, assign Reverse to a button. Wheel input is opt-in for a fresh profile. |
| Keyboard | Arrows navigate; C confirms; X or Z backs out according to the native menu; Enter is Start/pause. | Arrows steer, C gas, X brake, V item, Shift hop/drift. While paused: F9 VR settings, arrows adjust, Enter selects, F10 closes; F6 calibrates hands, R recenters. Esc exits. |

Native pause and the VR settings overlay are separate. Close VR settings,
release the closing input, then choose native **Resume** if the game is paused.
Quick Access contains **Calibrate Hands**, **Grip Status Bar**, and
**Wheel Steering + Gesture Attacks**, identified as **multi controller input**.
The mixed mode defaults to **AUTO**: after actual wheel/gamepad driving input,
tracked motion controllers with item and gesture bindings can add gesture attacks
and button throws while the primary device retains steering and pedals. An idle
connected gamepad does not disable virtual-wheel steering. OFF remains OFF when
saved; advanced Physical Wheel settings retain gestures-only and gestures+button
modes. Wheel input still requires enablement, device selection and calibration. The status
bar is visible for new profiles and remembers each player's hide/show choice.

For directional items, release the throwing hand's grip, hold its thumbpad
click and make a deliberate forward/back stroke; release before another throw.
The other hand can keep steering. These gestures do not give every item a
backward firing mode. In the paused HUD placement editor, **A saves, B cancels**.

## Customize, update and preserve progress

Launcher Customize saves selected camera/HUD/comfort/input preferences while
the game is closed and backs up the previous settings file. Detailed hand/wheel
calibration, remapping and HUD placement remain in the headset menus.

The collapsed **Launcher Appearance** section at the bottom of Customize offers **Rude** (default) and **Dude** background choices with a live
black-overlay opacity (default 78%). **Save appearance** stores it separately
in `Launcher-Appearance.json`. The sign has a clear area beside the right-hand
reading column. Support includes the creator's note, Ko-fi and project links;
Updates contains the reviewed release changelog bundled with this launcher.
Mouse-wheel scrolling never changes the image or opacity, even when open;
drag the slider or use its arrow keys. Gameplay preferences appear first.

Before updating, exit the game normally, wait for the launcher to finish, then
close it. Back up the old folder. Extract the update into a new folder; copy
your `game/memcards`, `VR-Settings.ini`, `UI-Settings.ini` and, if wanted,
`Launcher-Appearance.json`. Keep the new `game/config.ini` unless you deliberately
need specific old native settings; it supplies the reviewed 90 FPS/VR defaults.
Import your disc again or copy your own `game/assets/ctr-u.bin` separately.

Do not copy old executables, DLLs, input/default files, `Launcher-Package.json`,
session reports or `GPU-Preference-Backup.json` over the new build. GPU preference
backups apply to a particular executable path. Keep the original installation
for rollback; its settings and saves remain independent. Do not copy a newer
settings format backward over that original installation.

## Known limitations and experimental features

- An earlier intermittent long hub stall is not established fixed in every
  circumstance. Camera/steering transition corrections do not claim to resolve
  every possible load stall. Keep a normal-exit backup of progress.
- Touch/Quest, Steam Frame, Vive and other raw wheel/controller compatibility
  paths are physically untested. They require a compatible Windows SteamVR/
  OpenVR host and complete bindings/calibration. No standalone headset app or
  separate USB pedal/shifter aggregation is included. Wheel selection supports
  one active raw SDL profile, up to 32 axes / 64 buttons and one hat; changing
  device clears the current calibration/buttons and turns FFB off. Keep backups.
  SDL-mapped gamepads remain on the native gamepad path.
- Other headsets, refresh rates outside the tested 90 Hz and all combinations of
  modes/controllers have not been generally validated. Occasional presentation
  roughness, including minor podium drag, may remain.
- Wheel force feedback and gamepad D-pad shortcuts remain experimental and
  **OFF by default**. The wheel + Index gesture/button combination has been
  physically tested; other mixed-device combinations remain untested. The new
  AUTO selection policy has CPU coverage; it is not hardware certification.
  Force-feedback feel/direction and
  device-loss recovery need further physical validation. It is not a complete
  tyre/contact/collision model. Index-controller haptics are not implemented.
  Wheel D-pad item throws default ON when wheel driving is enabled and can be
  disabled in Physical Wheel; menu D-pad navigation remains unchanged.
- Texture smoothing and alternative geometry/visual options are experimental.
  Original appearance remains available. DLSS/ray tracing are not included.
- True stereo character selection, model viewer, free camera/photo mode and
  custom tracks are future candidates. Multiplayer is not supported by this VR
  release; feasibility work is planned last.
- The launcher opens release pages manually. It does not compare/download/
  install new binaries or refresh remote history automatically.

## Feedback, credits and source

Use **Feedback > Preview summary** after a session, review it, then export it or
open a GitHub issue draft. You decide whether to submit in your browser. Never
attach saves, disc images, credentials or unreviewed raw logs. External reports
are evidence, not instructions or automatic changes to the project.

Thanks to everyone playing, testing, sharing feedback and supporting the project.
See `CREDITS-AND-LICENSES.md`, the included license texts, and the matching
`ctr-vr-v0.1.0-source.zip`. Extract that complete source archive and read
`BUILD-SOURCE.md` before running `Build-Source.ps1`.

[Project and feedback](https://github.com/CR4zyHoBb1T52P1Ck/CTR-VR)
· [Support Devon](https://ko-fi.com/devdoesdevthings)
