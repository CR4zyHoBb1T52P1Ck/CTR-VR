# CTR VR

An unofficial Windows / SteamVR mod for Crash Team Racing: Turbocharged, with stereoscopic worlds, first-person driving, a customizable original-art HUD and one- or two-handed virtual-wheel controls.

**v0.2.1 — Creator Polish & Native Refresh Modes** is available. **144 Hz remains EXPERIMENTAL.** Download the [Windows package and complete matching source](https://github.com/CR4zyHoBb1T52P1Ck/CTR-VR/releases/tag/v0.2.1), read the [complete feature/release notes](docs/RELEASE_v0.2.1.md), [changelog](docs/CHANGELOG_v0.2.1.md) and [launcher guide](docs/DESKTOP_LAUNCHER.md).

This update bundles native timing and creator refinements since v0.2.0: OBS capture and presets, paused Photo/free-camera composition, automatic protected scene preparation, head-relative camera controls, grip world manipulation, a loaded-kart viewer, seven saved colour looks, clearer in-headset framing and controller handoffs. Photo opens in a gold-bordered 2D view of the PNG; P switches to stereo with a live viewfinder and L changes locked/head-follow capture. Index left pad top/bottom changes filter opacity; right pad top/bottom selects next/previous look. Creator > Open screenshots opens the active build's game/captures folder.

**90 Hz remains the default and visual reference. Native 80 is a fallback; native 120 has successful owner testing with OBS and in-game AA enabled.** Heavy tracks can still dip. **144 Hz remains experimental:** correct game speed does not establish 144 distinct world frames. The new portal-menu fix and guarded 144 window-presentation trim have CPU/build coverage; physical comparison is still pending. Earlier releases remain preserved. Follow the [80 / 90 / 120 / 144 setup guide](docs/FRAME_RATE_GUIDE.md): set actual headset Hz before launch, choose and save the corresponding launcher profile, then restart. The in-game FPS picker does not select headset Hz. Keep OBS and AA in the performance target.

## Play your way

- Stereo Adventure tracks, hubs and supported arenas; tracked native menus, results and supported cutscenes where appropriate.
- First- or third-person camera, recentering, comfort options and saved layouts.
- Valve Index thumbstick, hand-position and one/two-handed virtual-wheel driving, calibration, remappable buttons and directional item gestures.
- Xbox gamepad, keyboard and Logitech G920 input/calibration paths.
- Original-art/text/hidden HUD, 25 grouped widgets and paused placement tools.
- Player launcher with controls, selective preferences, Support, feature catalog, reviewed changelog, optional reviewed feedback and adjustable rendered homage background.

Physical coverage is strongest on Windows / Index, G920, Xbox and keyboard, including owner-tested native 120 with OBS/AA and Photo looks. Touch/Quest, Steam Frame, Vive and other wheel/controller profiles remain physically untested compatibility paths through a compatible Windows SteamVR/OpenVR host. Wheel steering + gesture attacks (multi controller input) defaults to hardware-gated AUTO, including motion-controller button throws. Force feedback and progressive pedal mode remain experimental, optional and OFF by default. Xbox/gamepad and wheel D-pad Up/Down throw items forward/backward by default for new profiles; saved OFF is retained. Toggle gamepad throws under VR Settings > Controllers. The current viewer isolates the loaded frozen kart/driver; animated full-roster viewing, stereo frontend selection, custom tracks and multiplayer remain future work. See the release notes for limitations, including the earlier intermittent hub stall.

## Install and preserve progress

Use the versioned Windows ZIP in a **new writable folder**, keep all files together, and verify its SHA-256 against the matching checksum file. Open **CTR VR Launcher.exe**, add your own compatible raw NTSC-U disc BIN, connect the headset/controllers, and choose **Play in VR**. No retail game data or personal saves are included. The first-launch headset guide explains controls.

Index right thumbstick **click** is Start/pause; left thumbstick **click** pauses and opens VR settings. Quick Access has hand calibration, grip-status visibility and Wheel Steering + Gesture Attacks (multi controller input). The launcher Controls page lists tested and untested input paths. Clutch-pedal/button reverse is separate from wheel D-pad weapons. Select other raw SDL wheels under Input Devices; device changes require fresh calibration and mapping. Launcher Appearance is collapsed at the bottom of Customize and ignores mouse-wheel opacity changes. See the [controls reference](docs/RELEASE_v0.1.0.md#essential-controls).

Back up the old folder with the game/launcher closed before updating. Move your own memory cards/settings selectively; keep new binaries, manifests, bindings and default configuration together. Follow the [update/rollback steps](docs/RELEASE_v0.2.1.md#install-update-and-roll-back).

## Build, credits and feedback

The matching source ZIP includes patched Turbocharged sources, the VR bridge, launcher/tooling, pinned OpenVR SDK and vendored SDL. Follow the [source-build instructions](docs/BUILD_RELEASE_SOURCE.md). Retail data is not needed for compilation/CPU checks. Byte-for-byte reproducibility is not claimed.

Launcher/tooling uses MIT terms; the native integration is GPL-3.0-or-later. Dependencies and artwork retain their own notices. Read the [credits and license inventory](docs/RELEASE_CREDITS.md) and included full texts. This free unofficial project has no affiliation or endorsement by the original game's owners, the Turbocharged team or Valve.

Use Feedback to preview/export an allowlisted summary and deliberately open a GitHub issue draft. There is no automatic upload, token storage or report-to-code automation. External testing evidence is reviewed with the owner before acting; see [community feedback boundaries](docs/COMMUNITY_FEEDBACK.md).

[Support Devon](https://ko-fi.com/devdoesdevthings) · [Project and issues](https://github.com/CR4zyHoBb1T52P1Ck/CTR-VR) · [Proposed updates](docs/PUBLIC_ROADMAP.md)

## Release repository

This public repository contains reviewed player documentation and release
records. Download both the Windows package and its named complete source ZIP
from Releases. GitHub's automatic source-code archives contain only this
documentation tree; see [complete corresponding source](SOURCE.md).
