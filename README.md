# CTR VR

An unofficial Windows / SteamVR mod for Crash Team Racing: Turbocharged, with stereoscopic worlds, first-person driving, a customizable original-art HUD and one- or two-handed virtual-wheel controls.

**v0.2.0 — The Streamer / Creator Update** is available. **Experimental Framerate Modes are in Testing.** Download the [Windows package and complete matching source](https://github.com/CR4zyHoBb1T52P1Ck/CTR-VR/releases/tag/v0.2.0), read the [release notes](docs/RELEASE_v0.2.0.md), [changelog](docs/CHANGELOG_v0.2.0.md) and [launcher guide](docs/DESKTOP_LAUNCHER.md).

This update adds a dedicated OBS capture window, saved recording presets, paused Photo composition, controller camera controls, grip world manipulation and PNG screenshots. Photo opens in a bordered 2D view of the PNG; P switches to stereo composition with a live 2D viewfinder and L changes locked/head-follow capture. Creator > Open screenshots opens the active build's game/captures folder.

**90 Hz remains the default and visual reference.** Optional 72/80/120/144 Hz modes still need testing; correct game speed does not guarantee smooth rendering. Keep OBS and AA in the performance target. The latest framing and Xbox shortcut default have CPU/build coverage and await physical comparison. v0.1.0 and v0.1.1 remain preserved. Stereo character/garage and model-viewer work remains on hold.

## Play your way

- Stereo Adventure tracks, hubs and supported arenas; tracked native menus, results and supported cutscenes where appropriate.
- First- or third-person camera, recentering, comfort options and saved layouts.
- Valve Index thumbstick, hand-position and one/two-handed virtual-wheel driving, calibration, remappable buttons and directional item gestures.
- Xbox gamepad, keyboard and Logitech G920 input/calibration paths.
- Original-art/text/hidden HUD, 25 grouped widgets and paused placement tools.
- Player launcher with controls, selective preferences, Support, feature catalog, reviewed changelog, optional reviewed feedback and adjustable rendered homage background.

The physically tested target is Windows 11 / Valve Index at 90 Hz and the supplied 90 FPS configuration. Other headsets/refresh rates are not generally validated. Touch/Quest, Steam Frame, Vive and other wheel/controller profiles are available as physically untested compatibility paths through a compatible Windows SteamVR/OpenVR host. Wheel steering + gesture attacks (multi controller input) defaults to hardware-gated AUTO, including motion-controller button throws. Force feedback and progressive pedal mode remain optional and OFF by default. Xbox/gamepad and wheel D-pad Up/Down throw items forward/backward by default for new profiles; saved OFF is retained. Toggle gamepad throws under VR Settings > Controllers. Multiplayer is not supported by this VR release. See the release notes for limitations, including the earlier intermittent hub stall.

## Install and preserve progress

Use the versioned Windows ZIP in a **new writable folder**, keep all files together, and verify its SHA-256 against the matching checksum file. Open **CTR VR Launcher.exe**, add your own compatible raw NTSC-U disc BIN, connect the headset/controllers, and choose **Play in VR**. No retail game data or personal saves are included. The first-launch headset guide explains controls.

Index right thumbstick **click** is Start/pause; left thumbstick **click** pauses and opens VR settings. Quick Access has hand calibration, grip-status visibility and Wheel Steering + Gesture Attacks (multi controller input). The launcher Controls page lists tested and untested input paths. Clutch-pedal/button reverse is separate from wheel D-pad weapons. Select other raw SDL wheels under Input Devices; device changes require fresh calibration and mapping. Launcher Appearance is collapsed at the bottom of Customize and ignores mouse-wheel opacity changes. See the [controls reference](docs/RELEASE_v0.1.0.md#essential-controls).

Back up the old folder with the game/launcher closed before updating. Move your own memory cards/settings selectively; keep new binaries, manifests, bindings and default configuration together. Follow the [update/rollback steps](docs/RELEASE_v0.2.0.md#install-update-and-roll-back).

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
