# CTR VR

An unofficial Windows native/SteamVR mod for Crash Team Racing: Turbocharged,
with stereoscopic worlds, configurable driving controls, original-art HUD,
Photo/freecam and Creator recording tools.

**v0.3.1 - Theatre and Creator Studio** is available. Download the
[Windows package and complete matching source](https://github.com/CR4zyHoBb1T52P1Ck/CTR-VR/releases/tag/v0.3.1),
read the [release notes](docs/RELEASE_v0.3.1.md), [Theatre/Photo controls](docs/THEATRE_CONTROLS.md)
and [launcher guide](docs/DESKTOP_LAUNCHER.md).

The final defaults patch includes the owner-approved Kart-relative REC placement,
verified in hubs and races. New installations receive it; existing saved layouts
remain authoritative. [Build and artifact verification](releases/v0.3.1/BUILD-VERIFICATION.json).

Record a race take, pause to save it, then open it in the launcher Theatre library.
Film using free/player cameras, a desktop gamepad or the **head/hand-tracked PC VR
viewfinder**. Scrub, reverse, mark In/Out, save shots/bookmarks and export clean
silent **landscape or phone-portrait MP4 clips**, up to 30 minutes within resource
limits. The takes retain observed draws, not a deterministic game-state simulation;
audio and unseen objects/effects may be absent. **30 fps is a workload-dependent
target**, not a locked distinct-frame-rate promise.

This milestone also adds interactive grabbable mod/Photo/Viewer panels, pointer
and hover explanations, a frozen **REC laser editor** with Kart/Head/World anchors,
controller-first take recording, portrait Photo/Creator output and three more
Photo looks. Creator Chase/PiP retains free position/scale, role swap and Gold or
Classic framing. In OBS record **CTR VR Capture**, not the headset mirror.

**90 Hz is the default/reference. Developer headset testing covers 80/90/120 Hz;
144 Hz remains EXPERIMENTAL.** Set headset Hz before launch and follow the
[refresh guide](docs/FRAME_RATE_GUIDE.md). Heavy races, Creator Capture and OBS can
still cause slowdowns; this release does not claim that all timing issues are fixed.
Standalone Frame VR also remains experimental and too slow for supported play.

Earlier working releases remain available as rollback. Full custom eight-racer
tracks, complete Garage, multiplayer and genuine game-state/audio replay remain
[roadmap work](docs/PUBLIC_ROADMAP.md), separate from the useful Theatre tools now shipped.

## Standalone Steam Frame preview and hardware hiatus

**22 November 2026:** the [last owner-tested standalone Frame build](https://github.com/CR4zyHoBb1T52P1Ck/CTR-VR/releases/tag/v0.3.2-frame-preview.1)
is available as an experimental update overlay, with complete matching source.
Read the [detailed progress/blocker report and personal update](docs/RELEASE_v0.3.2-frame-preview.1.md)
and [installation/rollback limits](docs/FRAME_PREVIEW_INSTALL.md).

Devon's Frame has stopped charging. Valve support has been contacted; repair/RMA
is unresolved. **Standalone Frame testing and development are paused indefinitely.**
This is the last standalone Frame update for the foreseeable future, with apologies
and thanks to everyone trying, playing and supporting the mod. No return date is
promised. Other PC/Index acceptance and testable projects may continue separately.

The final Cortex Castle test held a 100% game clock and 71.995 native updates/s,
but averaged 36.468 submitted world stereo pairs/s at a 72 Hz target. The owner
reported slightly steadier presentation; **native 72/90/120 Hz standalone VR is
not achieved**. The preview rejects 64.52% of opaque vertices while preserving
configured AA/100% eye scale. Later untested batching changes are excluded.

[v0.3.1 remains the stable PC/Index download](https://github.com/CR4zyHoBb1T52P1Ck/CTR-VR/releases/tag/v0.3.1)
and is unchanged. The preview needs an existing compatible Frame/Proton setup;
it is not a complete game, native SteamOS port or universal installer.

## Play your way

- Theatre library, free/player cameras, tracked head/hand filming, ranges/bookmarks/shots and clean MP4 export.
- Interactive Photo/Viewer tools, ten looks and wide/portrait PNGs.
- Stereo Adventure tracks, hubs and supported arenas; tracked native menus, results and supported cutscenes where appropriate.
- First- or third-person camera, recentering, comfort options and saved layouts.
- Valve Index thumbstick, hand-position and one/two-handed virtual-wheel driving, calibration, remappable buttons and directional item gestures.
- VR or headset-free flatscreen play with native keyboard/gamepad and calibrated wheels.
- Landscape Chase recording and freely positioned/scaled/swappable Gold-or-Classic PiP, with independent main recording HUD/status.
- Original-art/text/hidden HUD, 25 grouped widgets and paused placement tools.
- Player launcher with controls, selective preferences, Support, feature catalog, reviewed changelog, optional reviewed feedback and adjustable rendered homage background.

Chase/PiP, Photo, Theatre, menus and the final REC editor have owner acceptance on
their tested paths. Developer use covers Windows / Index and Frame PC streaming,
with gamepad/keyboard and prior G920 coverage. Quest 3 PC/SteamVR compatibility has
**community reports**, distinct from developer hardware testing. Broader hardware
and every control combination are not certified. No standalone headset installer
is included: the maintainer's preserved Frame flatscreen/Proton installation is
accepted locally, while standalone VR is separate and experimental.

Wheel steering + gesture attacks retains hardware-gated AUTO and saved options;
gamepad/wheel directional D-pad throws remain available. Force feedback and
progressive pedals remain experimental, optional and OFF by default, with broad
wheel/feel acceptance deferred. The loaded kart/driver viewer is distinct from a
complete 3D Garage. See the release notes for scope and limitations.

## Install and preserve progress

Use the versioned Windows ZIP in a **new writable folder**, keep all files together, and verify its SHA-256 against the matching checksum file. Open **CTR VR Launcher.exe**, add your own compatible raw NTSC-U disc BIN, connect the headset/controllers, and choose **Play in VR** or **Flatscreen**. No retail game data or personal saves are included. The first-launch headset guide explains controls.

Index right thumbstick **click** is Start/pause; left thumbstick **click** pauses and opens VR settings. Quick Access has hand calibration, grip-status visibility and Wheel Steering + Gesture Attacks (multi controller input). The launcher Controls page lists tested and untested input paths. Clutch-pedal/button reverse is separate from wheel D-pad weapons. Select other raw SDL wheels under Input Devices; device changes require fresh calibration and mapping. Launcher Appearance is collapsed at the bottom of Customize and ignores mouse-wheel opacity changes. See the [controls reference](docs/RELEASE_v0.1.0.md#essential-controls).

Back up the old folder with the game/launcher closed before updating. Move your own memory cards/settings selectively; keep new binaries, manifests, bindings and default configuration together. Follow the [update/rollback steps](docs/RELEASE_v0.3.1.md#preserve-verify-and-build).

## Build, credits and feedback

The matching source ZIP includes patched Turbocharged sources, the VR bridge, launcher/tooling, pinned OpenVR SDK and vendored SDL. Follow the [source-build instructions](docs/BUILD_RELEASE_SOURCE.md). Retail data is not needed for compilation/CPU checks. Byte-for-byte reproducibility is not claimed.

Launcher/tooling uses MIT terms; the native integration is GPL-3.0-or-later. Dependencies and artwork retain their own notices. Read the [credits and license inventory](docs/RELEASE_CREDITS.md) and included full texts. This free unofficial project has no affiliation or endorsement by the original game's owners, the Turbocharged team or Valve.

Use Feedback to preview/export an allowlisted summary and deliberately open a GitHub issue draft. There is no automatic upload, token storage or report-to-code automation. External testing evidence is reviewed with the owner before acting; see [community feedback boundaries](docs/COMMUNITY_FEEDBACK.md).

[Support Devon](https://ko-fi.com/devdoesdevthings) Â· [Project and issues](https://github.com/CR4zyHoBb1T52P1Ck/CTR-VR) Â· [Proposed updates](docs/PUBLIC_ROADMAP.md)

## Release repository

This public repository contains reviewed player documentation and release
records. Download both the Windows package and its named complete source ZIP
from Releases. GitHub's automatic source-code archives contain only this
documentation tree; see [complete corresponding source](SOURCE.md).
