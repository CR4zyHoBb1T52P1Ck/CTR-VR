# Standalone Frame preview overlay — installation and rollback

This is an experimental update for an existing compatible standalone Frame/Proton
installation. It is not a universal first-time installer or a native SteamOS port.
No headset testing or automatic deployment is queued while the maintainer's
charging fault/support case is unresolved. Read RELEASE-NOTES.md first.

## Existing working standalone installation

1. Quit CTR and close its compatibility process before copying files. Retain a
   complete working installation or verified backups of the old CTR-VR.exe,
   openvr_api.dll, input/ files and Steam launch profile. Preserve personal saves,
   config.ini, VR-Settings.ini, UI-Settings.ini, captures and race takes separately.
2. Verify SHA256SUMS.txt against the named downloaded ZIP. Extract this preview
   into its own folder. `python Frame-Profile-Tool.py --check` validates the staged
   payload only and never launches anything.
3. Copy the CONTENTS of overlay/ into the existing game's directory: CTR-VR.exe,
   openvr_api.dll and the included input/ JSON files. Do not replace your game
   data, saves or settings. Do not copy personal developer logs or old profile IDs.
4. Use a SEPARATE non-Steam standalone VR entry, with its target set to CTR-VR.exe
   and working directory set to that game's folder. Keep the already working
   Proton/compatibility and VR-title configuration. PC streaming must be disconnected
   for local standalone testing. Retain the independent flatscreen entry/profile.
5. On Frame, run `python Frame-Profile-Tool.py` from the extracted preview folder.
   It prints the matching environment/native launch options with a fresh session
   token and your home Desktop capture path. Paste that line into the VR entry's
   launch options. It does not register an entry, select/install Proton or launch
   CTR. The exact tested native flags are also readable in Frame-Profile.json.
6. Optional read-only verification after copying:

       python Frame-Profile-Tool.py --check --game-dir /your/existing/game/folder

   This checks only the allowlisted overlay files; it never edits that folder.
   A different file should be investigated rather than overwritten automatically.
7. Keep your tested headset refresh/configuration. The last measured run used
   72 Hz, 100% runtime eye scale and native AA setting 6. Interpolation and
   experimental pose smoothing are off. This does not achieve locked 72 Hz VR.
   The profile respects configured AA and does not edit Steam sharpening/quality.

This preview intentionally bypasses the stable Windows launcher's package hash
manifest when run directly through the standalone Steam entry. Do not try to use
the unmodified v0.3.1 launcher manifest as proof that this preview overlay matches
that stable package. The preview has its OWN RELEASE-MANIFEST.json and checksums.

## Preparing a new installation

A universal clean-device setup has not been qualified. Use the stable v0.3.1
package/instructions to prepare compatible base files and your own legally
supplied game data, or use an existing successful standalone deployment. Finish
any stable-launcher data preparation BEFORE applying this overlay. The overlay
does not contain the desktop launcher, base assets, a disc image, Proton or Steam.
Retain the platform-specific setup that is known to work on your device. There
is no promise that copying this ZIP alone creates a working local Frame title.

## Captures / diagnostics

The printed default capture root is your home Desktop/CTR VR CAPTURES through
Proton's Z: mapping. Create Photos, Videos and Race Takes subfolders there if
needed, or print a profile using an explicit Windows-style --capture-root value.
This helper does not create directories or install a capture encoder. Frame
photo/video encoding and complete capture-mode acceptance remain limited.

The default current-working-directory reports are frame-vr-perf-100-result.json,
frame-vr-perf-100-progress.jsonl and frame-vr-perf-100-lifecycle.jsonl. Normal Quit
gives the best chance of a final report. Steam Stop can leave only partial data;
that is not automatically a crash. Sparse GPU phase samples are enabled with the
same finite sample budget as the tested profile; the GAME has no automatic stop.
Review/redact private settings and logs before sharing. No automatic upload occurs.

## Rollback

With CTR closed, restore your own pre-update executable, DLL/input files and
Steam launch options, or use the untouched retained installation. Keep current
personal settings/saves unless you deliberately choose a backup. v0.3.1 remains
available unchanged for supported PC/Index use. Do not remove existing game data
or relink mutable settings to other installations. The later untested batching
candidate is not part of this update.
