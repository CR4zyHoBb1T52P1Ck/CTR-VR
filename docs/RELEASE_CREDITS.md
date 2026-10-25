# CTR VR credits and license inventory

CTR VR is an unofficial community project by Devon / DevDoesDevThings, built on
Crash Team Racing: Turbocharged and its contributors. Thank you to the players,
testers and supporters helping refine it. Original game names, characters,
artwork and trademarks remain associated with their respective owners; this
project does not claim affiliation or endorsement.

| Component | Distribution notice / source |
| --- | --- |
| CTR VR launcher and standalone tooling | MIT; `LAUNCHER_LICENSE.txt` in the Windows ZIP and `vr-mod/LICENSE` in source. |
| Native Turbocharged game integration and VR bridge | GPL-3.0-or-later; `game/LICENSE`, `game/THIRD_PARTY_NOTICES.md`; matching modified source in `turbocharged/`, `vr-mod/moving/`, `vr-mod/stationary/` and `vr-mod/moving/launcher.patch`. |
| Turbocharged base | Pinned revision in RELEASE-MANIFEST.json/SOURCE-REVISION.json; upstream https://github.com/CameronRedmore/Crash-Team-Racing-Turbocharged. Its source and notices are retained. |
| Valve OpenVR SDK | Pinned SDK revision; `game/OPENVR_LICENSE.txt`; matching SDK files and license in `vr-mod/.work/openvr/`. |
| SDL, PsyCross-derived code, PSn00bSDK headers, HIDAPI, stb and other native dependencies | Preserve `game/THIRD_PARTY_NOTICES.md` and `game/licenses/` verbatim. Individual source headers retain their notices. SDL source is included under `turbocharged/externals/SDL`. |
| Fuzzy Bubbles font | SIL OFL 1.1; copyright and terms beside the font in `game/assets/fonts/FuzzyBubbles-OFL.txt`. |
| Luckiest Guy font | Apache 2.0; full terms and attribution in `game/assets/fonts/LuckiestGuy-Apache-2.0.txt` and `LuckiestGuy-NOTICE.txt`. |
| Launcher icon | Drawn by the project's icon-generation script; source in `vr-mod/scripts/Build-LauncherIcon.ps1`. |
| Rendered launcher homage | Supplied and selected by the project owner for this launcher, replacing the earlier advertisement scan. Original JPEG SHA-256 `ccb037e64c2de1db721cdf4a95983fe812e52237216c42a4a8215e0890165505`; source `vr-mod/launcher/assets/Launcher-Homage.jpg`. Embedded unchanged with the owner's authorization. |
| Original retail disc content and optional Crash-a-Like font | Not distributed. Players supply their own compatible files; project software licenses do not license these materials. |
| Dude launcher variant | Owner-supplied friendly-wave rendition; `vr-mod/launcher/assets/Launcher-Dude.jpg`, SHA-256 `6fe8436a3d10e4c20d43559d3243b71421ce54f8ebc2154134699c3ce483af39`. Rude uses the sunglasses/hand-signal artwork listed above. Both are embedded unchanged and selectable in Launcher Appearance. |

The current launcher uses the owner's rendered homage; the earlier advertisement
scan is absent from the current source and newly built packages. This provenance
entry does not claim ownership or endorsement of third-party characters or
trademarks. The upstream `assets/dualshock.png` is retained from the
pinned base; its provenance is the upstream tree, without an invented separate
license grant. Keep this inventory with the exact release files.

The Windows package retains upstream Linux/AppImage license texts for provenance;
it does not ship a Linux AppImage runtime. Python, Visual Studio, CMake and
SteamVR are separately installed tools/runtime services, not bundled installers.

This inventory supplements the actual license texts; it does not replace them.
The source ZIP includes the modified native tree, bridge/tooling, pinned OpenVR
SDK, build script and instructions. Retail data, personal settings/memory cards,
runtime sessions and credentials are excluded.
