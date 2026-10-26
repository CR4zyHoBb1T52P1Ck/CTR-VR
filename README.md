# CTR VR

An unofficial Windows / SteamVR mod for Crash Team Racing: Turbocharged, with stereoscopic worlds, first-person driving, a customizable original-art HUD and one- or two-handed virtual-wheel controls.

**v0.1.1 is the day-one patch.** Download the [Windows package and complete matching source](https://github.com/CR4zyHoBb1T52P1Ck/CTR-VR/releases/tag/v0.1.1). Read the [patch notes](docs/RELEASE_v0.1.1.md), [changelog](docs/CHANGELOG_v0.1.1.md) and [Quest PC/SteamVR guide](docs/QUEST_PC_VR.md). The patch fixes a reproduced fresh-install config conflict that could keep gameplay on a tracked flat panel, and preserves virtual-wheel steering when one of two gripping hands briefly loses tracking. Physical Quest validation remains pending.

v0.1.0 remains available as the preserved original release. Stereo character/garage and model-viewer experiments are on hold and excluded from this patch.

## Play your way

- Stereo Adventure tracks, hubs and supported arenas; tracked native menus, results and supported cutscenes where appropriate.
- First- or third-person camera, recentering, comfort options and saved layouts.
- Valve Index thumbstick, hand-position and one/two-handed virtual-wheel driving, calibration, remappable buttons and directional item gestures.
- Xbox gamepad, keyboard and Logitech G920 input/calibration paths.
- Original-art/text/hidden HUD, 25 grouped widgets and paused placement tools.
- Player launcher with controls, selective preferences, Support, feature catalog, reviewed changelog, optional reviewed feedback and adjustable rendered homage background.

The physically tested target is Windows 11 / Valve Index at 90 Hz and the supplied 90 FPS configuration. Other headsets/refresh rates are not generally validated. Touch/Quest, Steam Frame, Vive and other wheel/controller profiles are available as physically untested compatibility paths through a compatible Windows SteamVR/OpenVR host. Wheel steering + gesture attacks (multi controller input) defaults to hardware-gated AUTO, including motion-controller button throws. Force feedback and gamepad D-pad shortcuts remain experimental and OFF by default; wheel D-pad item throws default ON when wheel input is enabled. Multiplayer is not supported by this VR release. See the release notes for limitations, including the earlier intermittent hub stall.

## Install and preserve progress

Use the versioned Windows ZIP in a **new writable folder**, keep all files together, and verify its SHA-256 against the matching checksum file. Open **CTR VR Launcher.exe**, add your own compatible raw NTSC-U disc BIN, connect the headset/controllers, and choose **Play in VR**. No retail game data or personal saves are included. The first-launch headset guide explains controls.

Index right thumbstick **click** is Start/pause; left thumbstick **click** pauses and opens VR settings. Quick Access has hand calibration, grip-status visibility and Wheel Steering + Gesture Attacks (multi controller input). The launcher Controls page lists tested and untested input paths. Clutch-pedal/button reverse is separate from wheel D-pad weapons. Select other raw SDL wheels under Input Devices; device changes require fresh calibration and mapping. Launcher Appearance is collapsed at the bottom of Customize and ignores mouse-wheel opacity changes. See the [controls reference](docs/RELEASE_v0.1.0.md#essential-controls).

Back up the old folder with the game/launcher closed before updating. Move your own memory cards/settings selectively; keep new binaries, manifests, bindings and default configuration together. Follow the [update/rollback steps](docs/RELEASE_v0.1.1.md).

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
