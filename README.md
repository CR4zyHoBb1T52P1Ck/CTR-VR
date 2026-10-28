# CTR VR

An unofficial Windows / SteamVR mod for Crash Team Racing: Turbocharged, with stereoscopic worlds, first-person driving, a customizable original-art HUD and one- or two-handed virtual-wheel controls.

**v0.2.3 — Creator Capture & Launcher Fixes** is available. **144 Hz remains EXPERIMENTAL.** Download the [Windows package and complete matching source](https://github.com/CR4zyHoBb1T52P1Ck/CTR-VR/releases/tag/v0.2.3), read the [release notes](docs/RELEASE_v0.2.3.md), [changelog](docs/CHANGELOG_v0.2.3.md) and [launcher guide](docs/DESKTOP_LAUNCHER.md).

This incremental update adds **Chase/headset PiP swapping**, applies pending Creator choices at Play, organizes Customize into **Current / Experimental / Legacy** options, and improves native90 capture setup/HUD reuse. Choose which view is large and the inset corner in Creator. OBS Window Capture must select **CTR VR Capture**; the main game/SteamVR mirror keeps the headset view. Capture/PiP default OFF, with saved choices retained.

**90 Hz remains the default/reference. Native 80 is a fallback; native 120 has owner testing with OBS and AA. Heavy tracks and Creator recording still dip. 144 Hz remains experimental.** The new diagnostics investigate remaining cost; this release does not claim locked90/120/144 performance. Follow the [refresh guide](docs/FRAME_RATE_GUIDE.md) and keep the same profile when comparing runs.

Photo/freecam, filters, grip manipulation and the frozen loaded-kart viewer remain. Supported models can try **experimental current-clip animation** in the viewer (V play/pause, N restart), with frozen fallback; physical animation acceptance is pending. This is not a full-roster viewer or automatic stereo garage. Quick Access reorganization remains a separate test candidate and is not merged here.

## Play your way

- Stereo Adventure tracks, hubs and supported arenas; tracked native menus, results and supported cutscenes where appropriate.
- First- or third-person camera, recentering, comfort options and saved layouts.
- Valve Index thumbstick, hand-position and one/two-handed virtual-wheel driving, calibration, remappable buttons and directional item gestures.
- Xbox gamepad, keyboard and Logitech G920 input/calibration paths.
- Optional landscape Chase recording and swappable headset PiP with independent main recording HUD/status.
- Original-art/text/hidden HUD, 25 grouped widgets and paused placement tools.
- Player launcher with controls, selective preferences, Support, feature catalog, reviewed changelog, optional reviewed feedback and adjustable rendered homage background.

Chase/PiP output has owner confirmation. Physical coverage is strongest on Windows / Index, G920, Xbox and keyboard, including owner-tested native 120 with OBS/AA and Photo looks. Touch/Quest, Steam Frame, Vive and other wheel/controller profiles remain physically untested compatibility paths through a compatible Windows SteamVR/OpenVR host. Wheel steering + gesture attacks (multi controller input) defaults to hardware-gated AUTO, including motion-controller button throws. Force feedback and progressive pedal mode remain experimental, optional and OFF by default. Xbox/gamepad and wheel D-pad Up/Down throw items forward/backward by default for new profiles; saved OFF is retained. Toggle gamepad throws under VR Settings > Controllers. The frozen viewer isolates the loaded kart/driver, with experimental current-clip playback for supported models. Full-roster viewing, stereo frontend selection, custom tracks and multiplayer remain future work. See the release notes for limitations, including the earlier intermittent hub stall.

## Install and preserve progress

Use the versioned Windows ZIP in a **new writable folder**, keep all files together, and verify its SHA-256 against the matching checksum file. Open **CTR VR Launcher.exe**, add your own compatible raw NTSC-U disc BIN, connect the headset/controllers, and choose **Play in VR**. No retail game data or personal saves are included. The first-launch headset guide explains controls.

Index right thumbstick **click** is Start/pause; left thumbstick **click** pauses and opens VR settings. Quick Access has hand calibration, grip-status visibility and Wheel Steering + Gesture Attacks (multi controller input). The launcher Controls page lists tested and untested input paths. Clutch-pedal/button reverse is separate from wheel D-pad weapons. Select other raw SDL wheels under Input Devices; device changes require fresh calibration and mapping. Launcher Appearance is collapsed at the bottom of Customize and ignores mouse-wheel opacity changes. See the [controls reference](docs/RELEASE_v0.1.0.md#essential-controls).

Back up the old folder with the game/launcher closed before updating. Move your own memory cards/settings selectively; keep new binaries, manifests, bindings and default configuration together. Follow the [update/rollback steps](docs/RELEASE_v0.2.3.md#install-preserve-and-build).

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
