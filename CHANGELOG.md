# Changelog

# v0.3.1 - Final REC placement defaults

- New installations now start with the owner-confirmed Kart-relative REC badge placement, visibility, distance, scale and orientation.
- The saved layout is shared between hubs and races; both contexts passed owner acceptance of the frozen grip/trigger laser editor.
- Existing saved layouts and personal settings take precedence. No profile, disc data, save or session log is distributed.
- The exact accepted v0.3.0 game executable, controls, Photo and Theatre runtime are retained unchanged.
- Updated full release overview, installation/update steps, controls and experimental-limit notes accompany matching Windows/source archives.
- v0.3.0 and all earlier releases remain preserved; this is a defaults/documentation patch, not a claim that performance limits are solved.

# v0.3.0 - Theatre and Creator Studio

- Integrated launcher Theatre library for frozen scenes and observed moving takes.
- Controller-first Record take on resume; pause seals the take, with clear REC/SAVED status.
- Free/player-anchored cameras, head/hand filming, pointer/timeline tools and independent tool-panel placement.
- Whole-take transport, frame/second seeks, reverse/rate, In/Out/loop, 64 bookmarks and eight saved shots.
- Clean silent local H.264 clips up to 30 minutes, in landscape or phone portrait; workload-dependent 30 fps target.
- Interactive mod and Photo/Viewer panels, hover explanations/highlights/haptics, title placement and mouse support.
- Explicit frozen REC laser editor with grip/trigger drag, size/tilt, Kart/Head/World anchors and safe Done/Cancel drafts.
- Frame Photo bumper height, D-pad filter/opacity and clearer face-button/keyboard guides; normal handoffs retained.
- Three additional Photo looks: Soft Pastel, Night Vision and Neon Arcade; existing look IDs preserved.
- Portrait Photo/Creator output, Chase/PiP framing/swap/gold style and paused custom-menu capture in OBS.
- Capture-buffer reuse, bounded allocation diagnostics and maintained render/query/copy refinements.
- Matching binary/source inventories, dependency/encoding checks, clean-stage privacy and checksum verification.
- Preserved PC flatscreen/gamepad/wheel play and owner-tested Frame local flatscreen installation.

144 Hz, standalone Frame VR, Chase/Stabilized recording, FFB and progressive pedals
retain experimental limits. Creator/OBS timing dips are not declared solved.
Custom full races, Garage, multiplayer and genuine game-state/audio replay remain
unfinished. No retail data, personal saves, credentials or captures are bundled.

[Full v0.3.0 release notes](docs/RELEASE_v0.3.0.md)

# v0.2.5 — Creator Capture & Performance Refinements

- Add headset-free flatscreen launch with native gamepad/keyboard and calibrated
  wheel support, plus independent flat wheel options. Flat Photo/motion remain pending.
- Add four-corner/free PiP placement, bounded resize, drag/numeric/VR placement
  controls and optional aspect-following thin Gold full-image frame. Keep Classic.
- Refresh Chase static scenery/sky/camera on same-generation world recapture;
  regression now exercises actual preparation and upload together.
- Retain bounded Chase buffer capacity and maintained HUD/render/capture cleanup,
  including per-pass widget raster reuse and idle capture work avoidance.
- Expand reviewed session/launch identity, sampling coverage and numeric capture/
  fallback/buffer diagnostics. Keep analysis offline and sharing deliberate.
- Advance actual custom-track background preload and mandatory root-qualified
  native preparation. No playable courses or checksum bypass are enabled.
- Preserve driving ownership, Photo/looks, HUD layouts, calibration, AA, saves
  and native timing policy.144 Hz remains experimental; heavy workloads still dip.

Owner accepted the scenery correction on the exact shipped game hash. Corrected
Cortex stress result94.6% mean clock at native 120/OBS recording+preview/AA; preceding
Gold N. Gin/Oxide results98.0%/96.8% are separate content-specific observations.
102 native tests pass/one optional skipped,15 track suites,362 launcher checks.

# v0.2.4 â€” PiP Menu Fix

- Show the selected Chase/headset large-view choice immediately in the VR PiP
  menu; share capture-action classification between input and label formatting.
- Allow A or Right to open the layout page and explain output after resume.
- Select new Feedback sessions on refresh and display local time, measured
  refresh/native rate and short report ID.
- Add reviewed launch/exit context, explicit missing/conflicting receipt status,
  optional OBS/video observations and compact issue drafts with manual full-JSON
  attachment. No automatic uploads or render-loop logging.
- Include offline evidence review, recovery and read-only audit/provenance tools
  in the complete matching source.
- Retain driving ownership, calibration, bindings, Photo, capture compositing,
  AA and timing algorithms. Owner confirmed the menu fix and swapped output.

Remaining: native 90/120 recording dips and demanding-race slowdowns; 144 Hz
remains experimental. No general performance fix or broad hardware acceptance
is claimed by this patch.


# v0.2.3 â€” Creator Capture & Launcher Fixes

- Add optional Chase/headset PiP view swapping at either supported inset corner.
- Apply pending Creator preferences at Play; retain failed saves and separate
  explicit timing confirmation.
- Enable guarded capture-idle and shared HUD-query optimizations for native90
  Creator world rendering, retaining recording quality and native AA.
- Group Customize and label current, experimental and superseded settings;
  retain saved legacy profiles and scroll-safe preference controls.
- Add bounded numeric capture-presentation subphase diagnostics for remaining dips.
- Include experimental safe current-clip animation in the loaded-kart viewer,
  with frozen fallback and unchanged gameplay/Photo input handling.
- Document native80/90/120 usage, experimental144/recovery, OBS source selection,
  PiP HUD behavior, screenshot location, update/rollback and complete source.

Known: native90 recording and demanding120 tracks may still dip.144 race
performance is experimental. Animation playback physical acceptance is pending.


# CTR VR v0.2.2 â€” Chase Camera & Picture-in-Picture

- Add optional recording-only Chase with bounded smoothing, transition/teleport
  resets and its own full captured kart/driver/wheel geometry and sorting.
- Add Off/Bottom-left/Top-left headset-eye PiP. Composite one colour copy into the
  existing capture output/PNG; no additional camera render or target.
- Reuse Creator cadence, FOV, output presets, recording HUD/status and shortcuts.
- Preserve Photo, controls, input ownership, native timing, AA and the v0.2.1 baseline.
- Use eye fallback when pose/body/wheel capture is unavailable; isolate Chase GL
  failures. Add bounded Chase/PiP counters to reviewed Feedback.
- Clarify OBS must capture **CTR VR Capture**; the main/SteamVR mirror stays the
  headset view and Primary mirror Capture rate is only a pacing option.
- Owner confirmed Chase/PiP output. The144 test still missed render cadence and
  included411 eye-fallback frames;144 remains experimental, with90/native120 the
  normal comparison targets. See release notes for exact evidence and limits.
- Stage Quick Access organization for the next workblock, without changing it here.

359 checks passed;two optional skips. Windows and complete matching source are
packaged separately from personal settings, saves, screenshots and retail data.


# CTR VR v0.2.1 â€” Creator polish and native refresh modes

**144 Hz remains experimental. 90 Hz is the default; native80/120 usage is documented in FRAME_RATE_GUIDE.md.**

- Bundle optimized native-rate and native120/144 clock-recovery options, retaining baseline90 and legacy experiments. Preserve AA, OBS use, configured FPS and calibration.
- Reduce redundant native window presentation on eligible144-Hz recovery world frames. Retain native drawing/VRAM/HUD and original panel/90/120 paths. Add skip counters; full144 remains unverified.
- Fix portal/race menus waiting for all Index controls to become neutral together; quarantine held entry commands independently. Keep native/wheel priority, held-Start rejection and tracking guards.
- Refine Photo return, automatic preparation and protected pre-pause textures; retain manual Resume and gameplay ownership.
- Add exact bordered2D PNG framing, stereo viewfinder, clear lock/follow state, view-relative navigation, hardware controls, world-grip manipulation and the frozen loaded-kart viewer.
- Add seven saved Photo looks with opacity, shared Photo/PNG colour processing, Original bypass and bounded fallback resources. Left Index pad top/bottom changes opacity; right top/bottom changes look. Clarify keyboard controls.
- Retain landscape OBS presets, recording-only HUD/status, primary mirror cadence/Dark and experimental stabilized-forward recording.
- Retain one/two-handed steering, occlusion recovery, wheel/pedal calibration/reverse, gamepad/wheel directional items, hardware-gated wheel+motion attacks and controller-loss pause refinements.
- Retain optional bounded spring/damper/turbo force feedback and default-Off analog cruising pedals, with physical/hardware limits stated.
- Preserve personalized HUD, saves, controls and launcher appearance. Expand numeric menu/cadence feedback without automatic uploads or report execution.

81 native,152 launcher and118 Python checks pass;two optional checks skip. Owner-tested creator/native120 foundations are distinguished from new portal/144 regression coverage. Quest/other hardware and full144 remain unverified. Full-roster animation, stereo frontend, smooth chase capture, custom tracks and multiplayer remain future work.


# CTR VR v0.2.0 â€” The Streamer / Creator Update

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


# v0.1.1 â€” day-one stereo-world and virtual-wheel fixes

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
