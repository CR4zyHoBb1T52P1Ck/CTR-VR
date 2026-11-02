# CTR VR v0.2.5 — Creator Capture & Performance Refinements

An incremental update for Creator recording, free Picture-in-Picture layout,
flatscreen play and measured rendering cleanup. Includes the Chase scenery
refresh correction confirmed by the owner. **144 Hz is still EXPERIMENTAL.
Demanding races and Creator recording can still run below full game speed.**

## Changes since v0.2.4

- **Play in VR or flatscreen.** Choose the launch mode in Play. Flatscreen uses
  native gamepad/keyboard input plus the calibrated steering-wheel bridge without
  starting a headset session. Independent flat wheel options cover sensitivity,
  deadzone, pedal/reverse threshold and directional items. Existing VR calibration
  and HUD settings are retained. Flat Photo/freecam, VR customization overlays
  and motion-controller/gesture flatscreen play are not included yet.
- **Freely place and scale PiP.** All four corner snaps plus a free position,
  10–60% requested width, launcher drag/resize diagram and numeric controls. Live
  placement has its own VR submenu and grip controls. Swap which existing view
  is large; the headset keeps its gameplay camera.
- **Optional Gold full-image frame.** A thin gold border follows the inset
  source aspect, showing the complete image without added bars, cropping or
  stretching. Tall eye views shrink to fit the output. Classic 16:9 fit remains
  the default. Bars already inside the source scene cannot be removed this way.
- **Correct Chase scenery after recovery.** Countdown/menu recovery can recapture
  a fresh world in the same resource generation. Chase now refreshes its static
  mesh, sky, sort bounds and camera anchor together. This fixes the observed
  stale/missing Cortex Castle scenery while preserving the current headset view.
- **Bounded render/capture refinements.** Maintained native profiles reduce
  redundant HUD queries/state/uniform setup and reuse widget setup within one
  immediate eye/editor pass. Retained-world drawing avoids irrelevant native
  flat-camera work; conservative view culling retains its fail-open behavior.
  Capture cadence skips idle setup, and Chase retains bounded spare vertex
  storage rather than reallocating for every new object-count high. The original
  rendering path remains available where eligibility is unknown. These changes
  do not lower AA, skip simulation/audio or promise a fixed FPS gain.
- **More actionable diagnostics.** Per-session identity/context, explicit launch
  flags, profiler sampling coverage, widget reuse, Chase fallback reasons,
  buffer growth/capacity and presentation subphases. Full reports are allowlisted
  and reviewed locally. OBS recording/preview observations remain explicit user
  declarations. Missing/conflicting evidence stays visible; nothing uploads
  automatically. Offline analysis runs outside racing rather than adding a
  live text-processing workload.
- **Source groundwork for custom tracks.** Real background paired-file preload,
  selected-root opened-handle checks and mandatory completed-root checks at native
  preparation, plus owned queue/GPU/save-isolation CPU proofs. **Custom tracks
  are not playable in this release.** A supplied XDELTA still requires its exact
  original source bytes; this update does not make patches universal.

## Creator recording and PiP

1. Open **Launcher > Creator**. Enable Capture window, choose Chase, resolution,
   30/60 updates, FOV and recording HUD/status. Select **Use Chase + PiP** if the
   saved layout is inactive. Choose the large view, inset corner/free position,
   size and **PiP frame style**. **Save creator settings** before launching.
2. Drag the diagram to move the inset; drag its bottom-right handle to resize.
   With diagram focus, arrows nudge and +/- resize; numeric controls provide exact
   placement. The diagram is framing guidance, not a live preview. It uses the
   latest local eye dimensions when available, otherwise a square guide.
3. During VR play open **F9 > Creator / Capture > Recording Layout / PiP**.
   Up/Down selects a row; A/Accept or Left/Right changes choices. **Move / Resize
   PiP** contains placement/size controls and the labelled grip interaction.
   **PiP Style** switches Classic/Gold. Capture Reset is on the Creator parent
   page so the compact layout page keeps every row visible.
4. In OBS choose **Window Capture > CTR VR Capture**. Chase changes that separate
   recording window; the game/SteamVR mirror remains the headset view. Resume
   gameplay to see the actual layout. Menus/loading, Photo and eye fallback use
   their existing paths rather than duplicating the inset.
5. **Recording HUD = Hidden** and **Recording input status = Hidden** hide main
   mono/Chase overlays. They do not erase the headset HUD baked into an eye/PiP
   image. Use HUD Layout Visibility to hide the currently selected headset widgets
   without changing their individual choices, or disable PiP for HUD-free output.

Eye Fill/Fit copy an existing eye. Clean mono, Stabilized and Chase add one scene
render at capture cadence. PiP reuses the existing images; swapping adds copies
and a small scratch target, not another scene render. Primary desktop preview
**Off / black** suppresses that optional mirror while CTR VR Capture stays live;
keep the main game window open for keyboard/input focus. OBS preview is a separate
cost. Hiding/minimizing the actual capture output is not promised to preserve OBS
Window Capture on every setup. Eye Fill/Fit remain the inexpensive fallback.
Chase has no wall-collision avoidance and can use eye fallback when required
pose/body/wheel geometry is missing.

## Retained controls, Photo and model tools

Index thumbstick, hand-position and one/two-handed virtual-wheel steering,
calibration, remaps, mixed wheel/gesture attacks and neutral controller handoffs
remain. Xbox/gamepad and wheel D-pad Up/Down support forward/back item throws
where enabled; saved OFF choices stay OFF. G920 calibration, braking/reverse,
steering options and native gamepad fallback are retained. Force feedback remains
experimental, optional and OFF by default, with conservative 10% initial gain and
25% cap; broad motor/feel acceptance is not established. Progressive calibrated
pedal cruising is also optional/experimental with original digital throttle
retained; boosts are not simulated by assigning velocity or clamping speed.

Paused Photo/freecam retains automatic scene/texture preparation, orbit/free
movement, live headset tracking, head-relative movement, grips to drag the world,
two-hand scale, visibility groups and bounded PNG capture. Its exact 2D viewfinder
is the composition reference; P changes preview and L changes lock/head-follow.
PNG output is **game/Captures** in the installation used. Space, right motion
trigger or the displayed gamepad/wheel capture button requests a screenshot.
Controls are displayed around the viewfinder and remain outside the PNG.

Photo looks retain left Index thumbpad Up/Down for opacity and right Up/Down for
next/previous look. Keyboard [ / ] selects looks, comma/period adjusts strength,
O restores Original. Gamepad Photo D-pad selects looks left/right and opacity
up/down; thumbsticks move the camera. Original/0% bypasses effects. The loaded
kart/driver/wheels viewer retains frozen fallback and experimental bounded current-
clip animation for supported models; it is not a full roster browser or automatic
stereo garage/character-selection replacement. These controls are VR Photo paths.

## Refresh rates, evidence and compatibility

Set actual headset refresh before launching; save the matching profile in
**Customize > Headset timing** and restart after a refresh change. The in-game
FPS menu does not set headset Hz; the launcher coordinates an effective process-
local native rate and retains saved FPS/calibration. Keep Native 3D and native game
Mirror mode off. Follow the [refresh guide](FRAME_RATE_GUIDE.md).

- **80 Hz:** Current Native, where the headset/transport exposes80. Earlier
  developer-tested lower-load option.
- **90 Hz:** default/reference with headset at 90; Current Native also follows90.
  Keep the same profile when comparing runs.
- **120 Hz:** Current Native, with developer testing under OBS and AA. Recommended
  higher-refresh path when the chosen track/capture workload has enough headroom.
- **144 Hz:** EXPERIMENTAL. Recovery can preserve game time while visible render
  cadence remains lower; neither proves locked 144 world rendering.72 remains
  physically untested. Older fixed90/interpolation profiles are legacy comparisons.

Latest corrected Cortex Castle native 120 stress run:113.464FPS/94.6% mean game
clock,114/216 under-cadence windows,12,553 actual PiP frames, zero submission/pose/
capture errors, clean exit. Owner confirmed restored scenery. Earlier N. Gin
and Oxide runs on the preceding Gold build averaged98.0% and96.8%, with complete
Chase scenery in sampled footage. OBS recording/preview and AA were enabled in
these reports. Tracks, race state and source differ: these are observed results,
not a controlled per-edit improvement, every-track ranking or hardware guarantee.
No new Photo entry occurred in the final Cortex report; prior Photo/input
acceptance is retained, not inferred from these race-only runs.

Developer headset testing covers80/90/120. **Quest 3 PC/SteamVR compatibility has
community reports relayed by the maintainer**; broader Touch/gesture coverage and
Quest 3S are not independently established. Steam Frame preparation is planned;
there is no tested Frame or standalone Quest/Frame build. Multiplayer, theatre
replay and playable custom tracks remain development work.

## Install, preserve and build

Download **ctr-vr-v0.2.5-windows-x86.zip**, verify **SHA256SUMS.txt**, and extract
into a **new writable folder**. Keep binaries/manifests/bindings/defaults together.
Open **CTR VR Launcher.exe** and supply your own compatible raw NTSC-U disc BIN.
Choose Play in VR or Flatscreen. No retail data, personal settings/saves, captures,
credentials, private sessions or debug databases are included.

Keep the complete old installation as rollback. With game/launchers closed, back
up and selectively transfer your own settings/memory cards; keep the new runtime
files and manifests. Do not replace a lone EXE inside another release. Existing
photos stay in their original installation. The accepted v0.2.4 release remains
available; the tested scenery-correction installation is also preserved locally.

The named **ctr-vr-v0.2.5-source.zip** contains complete corresponding modified
native/VR/launcher sources, pinned inputs, licenses and build instructions. GitHub's
automatic Source code ZIP/TAR contains only the public documentation tree. Use
**BUILD-SOURCE.md** from the named complete source asset. Matching source is
supplied; byte-for-byte reproducible builds are not claimed.

The game EXE is identical to the owner-tested scenery correction. Only launcher
release identity/documentation is promoted. Validation:102 native CPU tests pass,
one optional font test skipped;15 guarded track suites including 118 paired-file
host checks;362 launcher assertions; display-only layout checks and clean package/
source integrity/privacy audits. CPU checks are not headset/motor acceptance.
