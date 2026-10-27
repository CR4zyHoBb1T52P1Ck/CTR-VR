# CTR VR v0.2.1 — Creator polish, native refresh modes and control refinements

**144 Hz remains EXPERIMENTAL.** 90 Hz is the default/reference. Native 80 is a fallback and native 120 has successful owner testing with OBS and in-game AA active; performance varies by track, PC and recording settings. Correct game speed does not prove full headset-rate rendering. Read the [80 / 90 / 120 / 144 setup guide](https://github.com/CR4zyHoBb1T52P1Ck/CTR-VR/blob/main/docs/FRAME_RATE_GUIDE.md).

This bundles the Photo, free-camera, loaded-kart viewer, controller handoff and native timing work since v0.2.0. Earlier releases remain available. The new portal-menu fix and 144 presentation trim have build/regression coverage; their physical comparison remains pending at publication. The project owner requested publication with that experimental status retained.

## Install, update and roll back

Download **ctr-vr-v0.2.1-windows-x86.zip**, check SHA256SUMS.txt and extract into a **new writable folder**. Keep the complete package together. Open **CTR VR Launcher.exe**, import your own compatible raw NTSC-U CTR BIN and launch through Play in VR. No retail disc or personal saves are distributed. Windows and a compatible SteamVR/OpenVR PC connection are required; this is not a standalone Quest port.

Close the game/launcher and preserve the entire old folder before updating. Copy your own VR-Settings.ini, UI-Settings.ini, optional Launcher-Appearance.json and game/memcards into the new installation. Re-import/reuse your disc. Retain the new binaries, action manifest, bindings, defaults and game config. Select/save timing for your actual headset rate before Play; do not blindly copy a timing preview for another rate. Each installation saves separately. Old photos remain in the old game/captures. Return to the complete old folder for rollback.

## Steering and motion controls

- **Index driving:** thumbstick, hand-position and calibrated virtual-wheel modes; one/two-handed grip steering, hand swapping, centre/axis locks, sensitivity/deadzone and remappable driving buttons. Initial hand setup and paused recalibration remain. Brief one-hand occlusion retains the usable steering reference. Real headset/focus loss retains neutral output and manual Resume safeguards.
- **Physical wheels:** G920 selection, calibrated steering/pedal travel, strength/deadzone, assignments and mixed-controller handoffs. Clutch-pedal/button reverse is separate from wheel D-pad Up/Down directional item throws. Other raw SDL wheels can be selected, calibrated and mapped as untested hardware; force-feedback compatibility is not assumed.
- **Wheel steering + gesture attacks (multi controller input):** Quick Access defaults to hardware-gated AUTO. A real wheel/gamepad driving owner supplies steering/throttle while motion controllers supply directional gestures or an item button. Ordinary virtual-wheel gripping can reclaim Index driving. Grips plus triggers do not act as a Pause chord.
- **Gamepad and keyboard:** Xbox/native gamepad driving and menus; D-pad Up/Down forward/backward item throws with a saved toggle. Keyboard arrows steer/navigate, C accelerates/confirms, X brakes, V uses items, Shift hops/drifts and Enter is Start/pause. Native item restrictions and saved remaps remain.
- **Input return:** Photo closes with one neutral handoff and per-control held-input quarantine. In-game portal/race menus now quarantine held entry commands independently, allowing fresh A/B while a stick remains displaced. Native/gamepad priority, wheel Start rejection, loading/setup and tracking guards remain. No automatic Resume is generated.

Index **right thumbstick click** is native Start/pause; **left click** pauses and opens VR settings. Either stick navigates native menus, either A confirms and either B goes back. Quick Access contains hand calibration, status visibility and mixed-controller input. The launcher Controls page retains a permanent reference.

## Optional force feedback and progressive pedals

**Force feedback is experimental and OFF by default.** In paused VR Settings open **Input Devices > Wheel Force Feedback**, or Physical Wheel > Force Feedback. Supported haptics provide return-to-centre spring, turn resistance/damper and optional turbo pulses. Master gain defaults to 10% and is capped at 25%; conditions and finite-duration effects are bounded. Unchanged condition uploads are cached, effects stop outside safe owned wheel driving, and haptic failure retains input. This is an optional steering-effect model, not complete surface/collision simulation on every wheel. Begin with the low default. No motor was automatically activated during release preparation.

**Progressive pedal cruising is experimental, OFF by default.** Enable it in Creator or Physical Wheel > Pedal Mode after calibrating travel. It uses the native analog cruising-target path; original digital throttle remains available. It does not assign velocity, clamp boosts or reset calibration. Brake, clutch reverse, boosts, steering settings and other input owners retain their native paths. Full hill/boost/travel acceptance remains pending.

## Photo, free camera, viewer and filters

Load a single-player hub/race and Pause. Open **VR Settings > Creator / Capture > Photo scene / visibility > Enter Photo**, or close VR settings and use **Alt+F7**. Scene preparation and protected pre-pause texture capture are automatic; no pre-cache toggle is needed. If the protected copy is unavailable, Resume and Pause again. Gameplay stays frozen while headset tracking remains live.

- Orbit/free movement, distance, height, FOV, reset and scene visibility. This is a **paused composition free camera**, not a live flying spectator camera or cinematic-path editor. Captured geometry and movement bounds limit unseen surfaces.
- Head-relative sticks in stereo/head-follow; locked exact-2D composition follows the visible frame heading. One grip drags the world; two grips scale it within bounds. Camera Reset keeps the selected look.
- The gold-bordered **exact 2D PNG frame** opens by default. **P** switches to stereo plus a smaller viewfinder; **L** toggles locked/head-follow capture. Persistent camera/hardware labels sit outside the PNG. A stereo viewpoint can have a different perspective; the gold-bordered image is the composition reference.
- **Loaded-kart viewer:** View loaded kart / driver in the same menu isolates the current frozen kart/driver and separate wheel sprites, supports full orbit and reuses Photo controls. It is not an animated full-roster viewer or stereo character-selection garage.
- **Seven saved looks:** Original, Vibrant, Warm Postcard, Cool Dusk, Black & White, Sepia and Noir, with 0–100% opacity/strength. Photo stereo, viewfinder, capture and PNG share colour processing; text/borders remain unfiltered. Original/0% bypasses the effect. Bounded scratch targets release on exit; an effect failure falls back to Original. Looks do not colour gameplay or normal live recording.

### Photo controls

| Control | Action |
| --- | --- |
| Index left thumbpad: press top / bottom | Filter opacity +10% / −10% |
| Index right thumbpad: press top / bottom | Next / previous filter |
| Left bracket [ / right bracket ] | Previous / next filter |
| Comma , / period . | Opacity −10% / +10% |
| Letter O | Original look; camera unchanged |
| Index/Touch right trigger; Xbox X; configured wheel PNG button | Save PNG |
| Space / F12 / default Alt+F12 | Save PNG |
| Sticks; arrows / right-mouse drag | Camera movement/look, as labelled |
| Tab / Enter; controller Mode | Orbit/free camera |
| WASD; Q/E; PgUp/PgDn; minus/equals | Free movement; height; distance; FOV |
| Keys 1 / 2 / 3 / 4 / 5 | Kart+driver / wheels / other objects / scenery / sky |
| P / L; Index left/right stick clicks | Frame/stereo / locked/head-follow |
| Backspace / default Alt+F5; controller Reset | Reset camera/world manipulation |
| H / controller Help | Expanded help; core instructions remain visible |
| Escape / default Alt+F7; controller Return | Leave Photo, still paused; Resume manually |

Press a pad edge deliberately; touch/centre/held directions do not repeatedly change filters. Opacity blends the look with original colours, rather than making geometry transparent. Keep the game window focused for keyboard shortcuts. Detected hardware gets its Photo legend; wheel Photo buttons can be remapped in Creator. Custom SteamVR bindings may need the new optional Index Photo pad actions assigned; they are not reset automatically.

PNGs save in **game/captures** inside the active installation. **Launcher > Creator > Open screenshots** opens it. PNGs omit headset help. Protected VRAM addresses native pause-screen texture overwrites; missing captured geometry remains a limitation.

## OBS capture and recording HUD

Creator Capture provides a landscape **CTR VR Capture** window for OBS Window Capture, with 720p/900p/1080p, 30/60 updates, Fit/Fill, presets, FOV and shortcuts. **Eye Fill/Fit** copy an existing eye. **Clean mono** adds an independent scene view with recording-only HUD/status. **Stabilized forward** is an experimental native/kart view without head look; native/kart movement remains, and it is not a smoothed chase camera. Each mono mode costs a scene render at capture cadence; no extra game logic runs for it.

To hide all recording HUD, select a mono mode, set **Recording HUD = Hidden** and **Recording input status = Hidden**, then save with the game closed. Default **Alt+F2/F3** toggle them while recording; **Alt+F1** cycles views. Eye views include the headset HUD. **Quick Access > HUD Layout Visibility** hides only selected headset layout elements without rewriting individual widget choices.

Primary desktop mirror Live/Capture rate/Dark can reduce copies/swaps in optimized native profiles; keep its window open for input focus. The original mirror remains fallback. OBS preview is separate overhead, not another full game simulation. OBS and native AA remain part of the performance target and are not silently disabled.

## Refresh modes

With the game closed, set actual headset Hz in SteamVR/your PC connection software, choose the corresponding launcher profile in Customize, **Save launch settings**, then Play. Restart after a Hz change. The [full guide](https://github.com/CR4zyHoBb1T52P1Ck/CTR-VR/blob/main/docs/FRAME_RATE_GUIDE.md) explains diagnosis and legacy modes.

| Headset Hz | Launcher profile | Status / use |
| --- | --- | --- |
| 80 | Optimized native: 72 / 80 / 90 / 120 / 144 Hz | Native-rate fallback; earlier owner 80 testing succeeded. Broader device/configuration testing remains useful. |
| 90 | 90 Hz baseline | Default and visual reference; headset must also be 90 Hz. |
| 120 | Native 120 — tested optimized path; Optimized native also supports 120 | Owner-tested with OBS/AA. Heavy tracks can still miss cadence. |
| 120 under load | Native120/144 clock recovery | Experimental speed recovery with bounded native frames; rendered cadence can be lower. |
| 144 | Native120/144 clock recovery | **Experimental.** New redundant-window-present trim; full 144 rendering is not established. |

72 is a compatibility preview requiring hardware/runtime support. Legacy Match headset, fixed90 and interpolation modes remain comparison experiments. The game's higher flat-screen FPS choices do not select headset Hz. Launcher profiles set a process-local effective native rate without rewriting saved FPS/calibration. Do not change the in-game FPS picker during VR testing. 240 is outside the VR whitelist.

Recovery runs complete bounded native steps with retained input snapshots, without velocity edits or interpolating local wheel sprites. Normal speed/music can coexist with lower rendered FPS/reprojection. The 144 trim retains native scene drawing, AA and framebuffer-to-VRAM updates, and original startup/menu/pause/Photo/loading and 90/120 presentation. Feedback separates menu gates, delivered inputs, game time, rendering and omitted window passes.

## HUD, launcher, compatibility and feedback

Original-art/text/hidden HUD, 25 grouped widgets, saved hub/race/camera layouts, placement/scale/depth/yaw/tilt/visibility and paused editing remain. Camera/comfort includes first/third person, recentering, seating, smoothing, vignette and local-body visibility. Hub transition camera/steering continuity refinements remain included.

The launcher retains disc import, first-launch controls, customization, Creator/Support/About/Updates/Feedback, reviewed changelog, manual update links, Rude/Dude background selection and adjustable readability mask. Appearance stays collapsed at the bottom of Customize. [Support Devon on Ko-fi](https://ko-fi.com/devdoesdevthings).

Physical coverage is strongest on Windows / Index, G920, Xbox and keyboard. Native 120 and Photo looks have owner testing; the latest portal/144 changes have CPU/build coverage and await comparison. Quest 3/3S, Touch, Steam Frame, Vive and other wheels/controllers remain **physically untested compatibility paths** through Windows SteamVR/OpenVR. The earlier fresh-install stereo/config fix is included, without guaranteeing every transport/driver. Startup, menus, results and supported cutscenes normally use a tracked screen; assess stereo in playable single-player worlds.

The earlier intermittent hub stall is not established globally fixed. Full-rate 144, smooth chase capture, live spectator cameras, animated/full-roster viewing, stereo frontend selection, custom tracks and multiplayer remain incomplete/future work.

Feedback exports reviewed numeric evidence and optionally opens an issue draft. It does not automatically upload logs, execute external instructions, change code or store a GitHub token. Include Hz/profile, actual Creator view, OBS/AA, track and reproduction steps. Raw IDs, private paths, saves, disc data and screenshots are not automatically included. Community reports are reviewed with the owner before action.

## Source, checks and credits

**ctr-vr-v0.2.1-source.zip** contains complete matching modified native source, bridge, launcher/tooling, pinned OpenVR SDK, vendored SDL, build instructions and notices. GitHub automatic source archives contain only the public documentation tree; use the named source asset to build. Matching source is supplied; byte reproducibility is not claimed. Launcher/tooling are MIT, native integration GPL-3.0-or-later; dependencies retain their terms.

81 native, 152 launcher and 118 Python checks pass, with two optional skips. Coverage includes native clock/physics, steering/item ownership, Photo return/looks, portal entry and the guarded 144 window pass. These do not certify headset appearance, motor behavior or full-rate race performance. No game, SteamVR, OBS or motor was automatically launched during preparation. Included credits and full license notices remain with both packages.
