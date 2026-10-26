# CTR VR v0.1.1 — day-one patch

This patch addresses fresh installs remaining on the tracked flat screen during
gameplay and unexpected virtual-wheel interruption while both grips and throttle
are held. It retains the v0.1.0 feature set and excludes the experimental stereo
character/Adventure-garage/model-viewer work.

## Fresh-install stereo fix

The v0.1.0 package config listed `frame_rate=90` before legacy `60fps=1`. Both
settings wrote the same native option; the later legacy key selected 60 FPS.
The stereo-world readiness gate requires 90, so a new installation could remain
in panel mode even though the VR runtime and controls were running.

The native config loader now gives a valid explicit `frame_rate` precedence over
the legacy boolean, in either file order. Existing config files do not need to be
replaced. New packages omit the legacy key. A regression runs the actual native
config parser on the old package order and new package template, then verifies
stereo-world eligibility. The failing old behavior was reproduced before the fix.

This targets the reported Quest 3S/SteamVR symptom, but the reporter has not yet
supplied a session summary. Their exact cause and physical Quest behavior remain
unverified. The existing Windows OpenVR/SteamVR headset backend remains in use;
there is no standalone Quest APK or native Meta/OpenXR backend in this patch.

## Virtual wheel

Holding both grips and the trigger is not a pause shortcut. A pose dropout on
one gripping hand could invalidate the whole driving frame and request a safety
pause. The wheel now transfers to the other tracked gripping hand while preserving
its angle and current throttle. When the second hand returns, its newly valid pose
is rebased without treating the return as a teleport.

Losing all usable steering tracking still releases output and retains the existing
safety pause. Explicit thumbstick Start/settings clicks remain available. Tests
exercise the actual motion engine and ownership/output path, including the held
grip/trigger sequence, occlusion, hand return and genuine tracking loss. Physical
Index acceptance of this patch remains pending the owner's check.

The prior controls recovery is included: auxiliary wheel/gesture mode requires a
real driving owner, calibration clears stale auxiliary ownership, dormant startup
inputs cannot claim driving, and native menu focus recovery ignores driving-only
pedals/grips. Gameplay release barriers and manual Resume remain in effect.

## Installation and quick check

Extract the Windows ZIP into a new folder. Start **CTR VR Launcher.exe** at its
root, import your compatible retail disc data and launch through Play. Keep the
whole package together. The mod does not include game data.

For an upgrade, preserve the old folder. Copy your own `VR-Settings.ini`,
`UI-Settings.ini`, optional launcher appearance file and `game/memcards` into the
new installation while both are closed. Reuse/import your own disc. The corrected
loader also accepts the old explicit-90 config without editing private settings.
Each installation saves separately; avoid overwriting your archived working copy.

Startup movies, menus, loading and results normally use a tracked screen. Check
stereo after loading a single-player playable hub or race. If gameplay stays on a
panel, the new fixed hints identify game-rate, native-renderer or mirror blockers.
Use Feedback to review a summary containing actual game rate, world/panel counts
and readiness bits. Raw logs, private paths, serials, saves and disc data are excluded.

For Quest 3/3S, see [Windows SteamVR setup and reporting](https://github.com/CR4zyHoBb1T52P1Ck/CTR-VR/blob/main/docs/QUEST_PC_VR.md).
Physical coverage remains Index at 90 Hz, G920, Xbox and keyboard from earlier
owner tests. Quest and other headset/controller paths remain physically untested.
Use a 90 Hz SteamVR headset mode where available for this release's timing path;
other refresh rates have not been physically validated. No headset/SteamVR settings
are changed automatically.

## Retained limitations

- True stereo character selection/garage and the model viewer are pinned for
  later repair and are not in this patch. Their native screens remain available.
- Quest-specific transport, driver, GPU and timing problems may still require a
  focused follow-up after community evidence. GPU identity checks are retained.
- The intermittent long hub stall is not established globally fixed. The prior
  slowdown observations remain under investigation.
- Force feedback, alternate visual modes and broader device profiles retain their
  existing experimental/untested status. Multiplayer VR is future work.

Publication of this targeted patch was approved by the project owner. Automated tests do not
certify headset appearance, comfort, physical control behavior or performance.
