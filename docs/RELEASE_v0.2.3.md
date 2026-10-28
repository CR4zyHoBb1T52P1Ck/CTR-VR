# CTR VR v0.2.3 — Creator Capture & Launcher Fixes

An incremental update to Chase / Picture-in-Picture recording, launcher settings
and performance diagnostics. **144 Hz remains experimental. Native90 recording
dips and demanding-track slowdowns remain under investigation.** This update
does not claim locked90/120/144 performance across all tracks or hardware.

## Changes since v0.2.2

- **Swap the PiP views.** Creators can choose Chase large / headset small, or
  headset large / Chase small, at either supported left-hand inset corner.
  The swap reuses the two existing images; it adds image copies and a small
  scratch texture, not another scene render. Headset rendering stays unchanged.
- **Play now applies pending Creator choices before launching.** Previously a
  selected layout could remain unsaved and the game would launch its older saved
  choice. Failed saves retain the selection and prevent launch. Timing changes
  still require **Save launch settings** explicitly.
- **Native90 Creator capture can skip idle capture setup and reuse HUD queries**
  through the existing optimized paths. These were previously restricted to
  higher-rate/recovery paths. Recording resolution, output rate and native AA
  are retained. This does not automatically enable simulation recovery.
- **Customize is grouped and labelled.** Everyday camera/HUD settings and input
  controls come first. Timing choices say Current, Experimental or Legacy and
  explain their scope. Older/superseded comparisons can be revealed with a
  checkbox. Saved legacy selections remain visible and are never migrated.
  Preference pickers ignore accidental wheel scrolling. Appearance stays
  collapsed at the bottom.
- **More useful reviewed Feedback.** Capture preparation, draw submission, PiP
  copying and presentation have numeric CPU counters. Presentation is split into
  context entry, image copy/flush, window swap and native-context restoration.
  These help investigate remaining dips; they are wall CPU measurements, not
  independent additive frame costs or GPU timings.
- **Experimental loaded-model animation.** The loaded-kart viewer can use an
  owned, bounded copy of a supported model's current animation clip and material
  bindings. In that viewer, **V** plays/pauses and **N** restarts. Unsupported
  models keep the frozen-pose fallback. It does not run native actors or resume
  the game. Physical acceptance of animation playback is still pending. No
  roster browser or automatic stereo character-selection garage is included.

## Use Chase and PiP in OBS

1. With the game closed, open **Launcher > Creator**. Enable **Capture window**,
   select **Chase camera**, then choose resolution, 30/60 updates, FOV and
   recording HUD/status. Keep the same choices when comparing performance.
2. Enable **Chase picture-in-picture** at Bottom left or Top left. Choose
   **PiP large view**: Chase large / headset small, or Headset large / Chase small.
   Off disables the inset. Save Creator settings, or press Play to apply pending
   Creator preferences. During play use **VR Settings > Creator / Capture >
   Recording layout / PiP** for live changes.
3. In OBS select **Window Capture > CTR VR Capture**. The main game window and
   SteamVR mirror still show the headset view. Primary desktop mirror Capture
   rate/Dark only reduces that optional preview's copies/swaps. Keep the main
   game window open and focused for keyboard controls.
4. Load a playable single-player hub/race. The headset keeps its driving camera.
   PiP is applied only to successful Chase world output, not Photo, menus,
   loading or eye fallback. Both images preserve aspect; bars/cropping depend
   on the saved framing choice.

**Recording HUD = Hidden** and **Recording input status = Hidden** remove those
overlays from the main Clean mono / Stabilized / Chase recording. Eye mirrors
and the headset image in PiP include the headset's visible HUD/status. Use the
headset layout visibility control or turn PiP off if that image must be HUD-free.
Hiding the layout preserves which individual widgets are selected.

Chase adds one mono scene render at capture cadence. PiP does not add another.
Chase can fall back to the eye when required pose/body/wheel geometry is missing,
and has no wall-obstruction avoidance. Captured-world visibility and sprite wheels
still limit exterior views. Eye Fill/Fit remain the inexpensive fallback. OBS and
in-game AA remain the performance target; neither is silently disabled.

## Set headset refresh before launch

Close the game, set actual headset Hz in SteamVR/connection software, then choose
**Launcher > Customize > Headset timing** and **Save launch settings**. Check the
saved summary and restart after changing Hz. The native FPS picker does not set
headset refresh; do not independently select240 FPS during VR testing.

| Headset mode | Launcher choice | Status |
| --- | --- | --- |
|80 Hz|Current: Native|Earlier owner-tested lower-load fallback where the headset exposes80.|
|90 Hz|Current: 90 Hz reference|Preserved default and visual comparison reference. Creator recording can still cause dips.|
|90 Hz|Current: Native|Native-rate optimizations; keep this choice unchanged for an existing matched native90 test.|
|120 Hz|Current: Native|Owner-tested with OBS + AA. Heavy tracks/capture may still slow under load.|
|120/144 Hz|Experimental: Native clock recovery|Bounded native steps preserve game time when rendering falls behind; images can still repeat/reproject.|
|144 Hz|Native or clock recovery|**Experimental; not accepted as locked144 race rendering.** Return to120/90 when cadence is poor.|
|72 Hz|Native|Compatibility path; physical testing pending.|

Legacy match-headset, fixed90, interpolation, dedicated120 and dedicated144
choices remain for saved-profile compatibility and controlled comparisons.
Native headset rate is the maintained matching path. Recovery and Native are
different timing models; do not compare them as if only headset Hz changed.

The latest short native90 diagnostic run averaged86.08 rendered/logic FPS over
about27 seconds of measured world time. Capture-idle and HUD-query optimizations
were active. Presentation accounted for most measured capture CPU time, while
PiP copying was much smaller. These overlapping menu/gameplay measurements do
not establish a single cause or a reliable comparison against longer runs.
Further physical timing work is needed; zero submit errors does not prove smooth
full-rate rendering. Include perceived music/game-speed and image changes in reports.

## Retained controls, Photo and viewer features

- Calibrated Index one/two-hand virtual-wheel steering, native gamepad/keyboard
  driving, physical-wheel steering and clutch/button reverse. Wheel + tracked
  motion gesture/button attacks retain hardware-gated mixed input. Xbox and wheel
  D-pad Up/Down directional items respect saved toggles and native item limits.
- Custom HUD layouts and widget visibility, grip/input status and saved placement.
  Optional bounded force feedback and progressive pedal driving remain
  experimental; calibration and boost/brake/reverse paths are retained.
- Paused Photo/freecam with orbit/free movement, headset-relative motion,
  one-grip world dragging, two-grip scale, scene visibility, exact2D PNG framing,
  locked/head-follow views, filters and strength. Index right trigger, Xbox X,
  configured wheel capture button or Space can take a photo. Photo's visible
  help lists the active controls. Pre-cache prepares/releases automatically.
- Frozen loaded-kart viewer and existing Photo return/input handling. Experimental
  current-clip playback is separate from the accepted frozen viewer behavior.
- Photo/capture PNGs save in **game/captures** within the extracted installation.
  **Launcher > Creator > Open screenshots** opens that folder. Photo help and
  gold viewfinder border stay outside the saved image.

Windows SteamVR/OpenVR is required. Quest/Touch, Steam Frame, Vive and other-wheel
bindings remain compatibility paths with incomplete physical validation; this is
not a standalone headset app. True stereo frontend garage/character selection,
custom tracks and multiplayer are not provided by this update.

## Install, preserve and build

1. Exit the game and launcher normally. Preserve the complete old folder for
   rollback. Extract **ctr-vr-v0.2.3-windows-x86.zip** into a new writable folder.
2. Selectively copy your own `game/memcards`, `VR-Settings.ini`, `UI-Settings.ini`,
   `Launcher-Appearance.json` and, if desired, `Timing-Preview.json`. Import your
   own compatible NTSC-U CTR raw BIN or separately copy `game/assets/ctr-u.bin`.
   Keep deliberate native AA/config changes in your private backup and reapply
   them carefully; don't overwrite new binaries/defaults/bindings/manifests.
3. Keep the new package's executables, DLLs, inputs and manifest together. Don't
   copy old GPU-preference backups or raw session folders into the new build.
   Restore the full previous installation if needed; do not migrate new settings
   backward over its saved rollback profile.

The Windows package and complete corresponding **ctr-vr-v0.2.3-source.zip** are
included with checksums, revision manifest, credits and licenses. GitHub's automatic
source-code archive contains only the public documentation repository; use the
named complete source ZIP to build. Byte-for-byte reproducibility is not claimed.
No retail disc, personal settings/saves, private logs or development Git history
are shipped. Executables are unsigned. See BUILD-SOURCE.md in the source archive.

The desktop build passed382 CPU/offline checks with two optional skips. Offscreen
launcher previews checked the layout without starting the game/SteamVR/OBS. These
checks do not certify headset appearance, animation playback or frame-rate gains.

Use **Feedback > Preview summary**, review it, then export or open a GitHub issue
draft deliberately. No automatic upload or action on community reports occurs.
Please include track, headset rate, selected timing profile, Creator view/preset,
OBS/AA and whether slowdowns affect game speed, visible cadence or both. Keep
saves, disc data, credentials and unreviewed raw logs private.

[Project and feedback](https://github.com/CR4zyHoBb1T52P1Ck/CTR-VR)
· [Support Devon](https://ko-fi.com/devdoesdevthings)
