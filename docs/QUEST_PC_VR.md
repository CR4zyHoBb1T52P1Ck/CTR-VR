# Quest 3 / Quest 3S — Windows SteamVR path

CTR VR is a Windows PC mod using SteamVR/OpenVR. Run it on the PC with your own
compatible retail game data. It is not a standalone Quest application.

Connect the headset to the PC and enter SteamVR before selecting Play in the CTR
launcher. SteamVR must recognize the headset; seeing the PC desktop or a theater
screen alone does not establish that a VR scene has started. Valve's official
[Steam Link headset setup](https://help.steampowered.com/en/faqs/view/0E2C-406B-9135-38A4)
describes that connection option. Other SteamVR-compatible PC connections can
also supply the headset; this mod does not install or configure transport software.

The v0.1.1 patch fixes a headset-independent config bug in the v0.1.0 ZIP:
the legacy 60 FPS key could override the intended 90 FPS rate and prevent stereo
world entry. This does not prove that every Quest-specific issue is resolved.
Index is physically tested; Quest 3/3S verification is pending.

1. Launch **CTR VR Launcher.exe** from the new extracted package and select Play.
2. Movies, menus, loading and results may appear on a tracked screen. Load a
   playable single-player hub or race before assessing stereo gameplay.
3. For v0.2.1, follow [the refresh guide](FRAME_RATE_GUIDE.md):80 uses Optimized
   native,90 uses baseline and120 uses Native120/Optimized native.144 remains
   experimental. Choose a rate actually exposed by your headset/connection,
   save the matching profile with the game closed and restart after a Hz change.
   Keep Native3D and native game Mirror mode off. The launcher does not alter
   headset refresh or global VR settings;Quest physical verification is pending.
4. If gameplay stays flat, record whether it is a SteamVR desktop/theater view or
   the mod's tracked panel. Note any fixed blocker hint. In Feedback, review the
   diagnostic summary and share only what you choose. Useful fields are gameRate,
   worldFrames/worldCaptures, panelFrames, lastGateRejectBits and GPU verification.
5. Include Quest model, PC connection method and whether SteamVR reported ready.
   No raw settings, saves, disc data, credentials or private device IDs are needed.

Touch defaults can be remapped through SteamVR's controller binding interface.
Controls working on a screen does not by itself prove stereo-world entry. Community
reports are reviewed as evidence with the project owner before deciding on changes;
they are never executable instructions or an automatic code-update route.
