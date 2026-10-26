# CTR VR v0.2.0 — The Streamer / Creator Update

Experimental Framerate Modes are in Testing. Clean installs retain the 90 Hz baseline.

- Add a dedicated OBS capture window with Fit/Fill/Clean views, presets, resolution/rate choices and recording-only HUD/status.
- Add automatic paused Photo preparation, orbit/free camera, scene-group visibility and bounded PNG screenshots.
- Add Photo-only one-grip world translation, two-grip scaling, head-follow/locked capture and a default bordered PNG frame with persistent mode/camera labels, plus stereo composition with a live 2D viewfinder.
- Enable Xbox/gamepad D-pad Up/Down forward/backward item throws for new profiles, retaining saved Off and normal menu navigation.
- Add Creator > Open screenshots and show the game/captures location clearly.
- Protect pre-pause texture pages and allow valid paused race-intro composition.
- Refine Photo action return while preserving calibration, native controls and ownership.
- Add optional, default-Off native analog cruising-speed pedal mode; physical acceptance remains pending.
- Add optional matched-rate, fixed90 and interpolated render timing profiles; preserve native local kart/driver/wheel sprite animation.
- Reuse interpolation/HUD geometry, improve compositor handoff and repeat native menu/loading panels with fresh headset poses.
- Expand reviewed scalar Feedback timing/Photo/capture diagnostics without automatic uploads.

See release notes for physical-test limits, recorded stalls and experimental 72/80/120/144 Hz behavior. The stereo garage/model viewer and multiplayer remain out of scope.


# v0.1.1 — day-one stereo-world and virtual-wheel fixes

- Fix a fresh-install config conflict: `60fps=1` could override `frame_rate=90`,
  keeping supported gameplay on a tracked flat panel. Explicit frame rate now wins
  regardless of file order; fresh packages omit the ambiguous legacy key.
- Keep two-hand virtual-wheel steering and throttle active through a brief loss
  of one gripping hand, using the other tracked hand and preserving steering angle.
  Rejoining the second hand no longer counts as a teleport. Actual loss of steering
  tracking still neutralizes input and retains the existing safety-pause behavior.
- Include the earlier mixed-input ownership/rearming and native-menu recovery fixes.
  An unowned wheel pose cannot disable Index driving after calibration.
- Show actionable panel hints for game-rate, renderer or mirror blockers. Feedback
  adds allowlisted world/panel counts, readiness bits and actual game rate.
- Keep stereo character/garage and model-viewer experiments out of this patch.

The Quest 3/3S Windows SteamVR path is a compatibility target. This fixes a
reproduced headset-independent fresh-package defect; physical Quest verification
and confirmation of the community reporter's exact cause remain pending.

# CTR VR v0.1.0 changelog

First full public release following the retained alpha.1 history.

## Worlds and presentation

- Stereo Adventure worlds, race tracks, hubs and supported arenas, with
  original-art materials, animated actors/textures and tracked native panels.
- Headset-first startup, supported podium/intro presentation corrections and
  bounded native HUD capture.
- First/third-person camera, comfort smoothing, seating/recenter and local-body
  visibility options; corrected brief distant-camera recapture at hub boundaries.

## Driving and customization

- Index native-menu navigation and fixed pause/settings thumbstick clicks.
- Initial in-world hand calibration, independent button release/rearm and
  same-controller steering continuation across hub loads.
- Thumbstick, hand-position and one/two-handed virtual-wheel steering,
  configurable buttons, wheel guide and directional item gestures.
- G920 calibration, assignments and steering-strength adjustment; gamepad and
  keyboard control paths, with source handoffs.
- Wheel steering + gesture attacks (multi controller input) in Quick Access,
  defaulting to AUTO only with actual primary-device intent and fresh tracked
  item/gesture bindings. Includes motion-controller button throws; saved OFF is
  retained. The wheel + Index gesture/button combination has been tested.
  Force feedback and gamepad D-pad shortcuts remain OFF by default.
- Clutch-pedal/button reverse, independent wheel D-pad items (default ON when
  wheel driving is enabled), explicit raw SDL device selection and fresh-profile
  guards. Additional wheel hardware is untested.
- Touch/Quest, Steam Frame and Vive SteamVR compatibility bindings, explicitly
  untested, with other controllers remappable through the same action sets.
- Original-art/text/hidden HUD, grouped placement tools and independent layouts;
  grip-status visibility in Quick Access, visible for fresh profiles.

## Launcher and distribution

- Player-focused navigation, controls reference, first-launch headset guide,
  selective preferences with backup and reversible per-app GPU request.
- Dedicated Support, feature catalog and reviewed release changelog pages.
- Rendered homage background, separate saved opacity/visibility and right-side content
  placement that leaves the sign clear, with centered column headings.
- Rude (default) and Dude background choices preview live and save separately
  from gameplay settings. Appearance is collapsed at the bottom of Customize;
  scrolling cannot change either image selection or opacity.
- Reviewed allowlisted diagnostic export and optional browser issue draft,
  without raw-log upload, stored GitHub tokens or automatic report actions.
- Audited Windows/source packages, complete source-build inputs, credits,
  installation/update/rollback instructions and SHA-256 checksums.
- A separate public release repository and explicitly allowlisted corresponding
  source snapshots; private development history and operator data are excluded.

This changelog summarizes source changes, not a new certification of every
device/mode. Known limitations are in RELEASE-NOTES.md. Future roadmap entries
are not shipped features. The prior alpha tag is not replaced.
