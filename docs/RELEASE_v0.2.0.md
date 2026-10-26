# The Streamer / Creator Update

## Experimental Framerate Modes are in Testing

**CTR VR v0.2.0** adds recording tools, paused Photo composition and clearer screenshot access. **90 Hz is the default and visual reference.** Other refresh-rate profiles remain optional experiments, not a promise of smooth or validated operation on every headset.

Download **ctr-vr-v0.2.0-windows-x86.zip** for Windows. The named **ctr-vr-v0.2.0-source.zip** asset contains the complete matching source; GitHub's automatic source archives contain only the public documentation repository.

## Streamer capture

- A dedicated **CTR VR Capture** window for OBS Window Capture, with Eye Fill, Eye Fit and Clean landscape mono views.
- Fit/Fill framing, 720p / 900p / 1080p, 30/60 capture updates, saved presets and remappable shortcuts.
- Recording-only HUD/status choices in Clean view; the headset retains its own saved HUD layout.
- The existing main-window mirror remains the inexpensive fallback. Clean mono adds rendering work; OBS recording and in-game AA remain performance targets, not reasons to disable those tools.

Capture defaults Off. Open **Creator**, select a preset and save with the game closed. Alt+F1 cycles views; Alt+F2/F3 toggle recording HUD/status. OBS is not launched or configured automatically.

## Photo Mode and screenshots

Pause in a loaded single-player hub/race, including a valid race introduction. Open **VR Settings > Creator / Capture > Photo scene / visibility > Enter paused Photo**, or close VR Settings and use Alt+F7. Preparation is automatic; no cache switch is required. The level stays frozen, headset tracking remains live, and leaving Photo returns to native pause for manual Resume.

- Orbit/free camera, movement, mono-output FOV, reset and local PNG screenshots.
- Keys **1–5** independently show/hide kart/driver, wheel sprites, other captured objects, scenery and sky. These are group controls, not object picking.
- **Right A / Enter / Tab** switches orbit/free. In free mode, release grips once, then hold **one grip** to move the frozen world or **two grips** to scale around the midpoint. Scale is bounded 0.25x–4x; translation is bounded to 2 m. Reset clears this Photo-only transform, leaving game scale, physics and calibration intact.
- Photo opens with a clearly bordered **2D PNG view and LOCKED capture camera**. **L / modifier + Mode** switches to head-following capture. The current camera state is always labelled in the headset.
- **P / modifier + Help** switches between the large 2D PNG view and stereo composition with a smaller live 2D viewfinder. Both show the actual full-aspect PNG texture, a gold capture border and persistent mode/camera labels, independently of help visibility. This is the framing reference: a mono screenshot cannot equal both stereo eyes, lens distortion or the headset's display processing. Preview uses the selected capture cadence; a screenshot request forces a fresh render.
- **Index right trigger**, **Xbox X**, **G920 X**, **Space/F12** or the remapped screenshot action saves one bounded PNG. Index modifier is left trigger; Help is left B; Mode is right A. Xbox uses LT+Start for preview and LT+A for capture following.
- **Creator > Open screenshots** opens **game/captures inside the active launcher folder**. Each portable build retains its own photos; older photos remain in the folder of the build that made them. Images are never uploaded automatically.

The headset help lists the controls; **H / Help** hides it. Help/status stay out of clean PNGs. Captured geometry limits the original camera to 6 m and +/-75 degrees; unseen objects, backsides and effects can remain missing. Grip panning/scaling does not load new geometry.

## Controls and rendering refinements

- Xbox/gamepad D-pad **Up throws forward; Down throws backward**, using the same directional item path as the wheel. New profiles default On; an existing saved Off stays Off. Enable it under **VR Settings > Controllers > Gamepad D-pad Up/Down Throws**. Held directions fire once; menus retain normal navigation. Native weapon direction restrictions still apply. Steering, gas, brake and gesture assist retain their existing mappings.

- Preserve native local kart/driver poses and separately tagged wheel sprites during high-refresh interpolation, avoiding interpolation of changing wheel sprite corners.
- Protect texture pages before the native pause screenshot overwrites VRAM, addressing the frozen-area Photo texture corruption.
- Separate Photo eligibility from the driving mount so paused race introductions can compose safely.
- Improve Photo return with fresh action sampling and a bounded held-control release gate; retain saved calibration and driving ownership. Explicit F9 settings requests survive that drain.
- Reuse bounded interpolation storage, cached geometry on repeated headset poses and unchanged HUD quad geometry in the high-Hz path.
- Present the companion window before compositor handoff; repeat loaded native menu/loading-flag canvases with fresh HMD poses while their native updates stay at 90 Hz. True movies retain their native pacing. Raster flag animation is not synthesized, and synchronous loading can still stall.

An optional calibrated **native analog cruising-speed pedal** mode is included, Off by default. It uses the game's existing analog target-speed path, preserving digital mode, boosts, braking and reverse. It does not assign velocity or clamp boost speed. Physical sustained pedal behavior remains unverified.

## Experimental timing: please read

Choose the profile in **Customize > Timing Preview** with the game closed, set the headset refresh rate before launch, and restart after changing headset Hz. The launcher does not change SteamVR/headset settings automatically.

- **90 Hz baseline:** recommended reference and clean-install default.
- **Match headset:** optional native-rate preview for 72/80/90/120/144 Hz. 80 Hz had successful owner playtests; broader hardware/rate acceptance is incomplete. Raising the native simulation rate can exceed the available frame budget.
- **Fixed 90 game clock + independent VR render:** preserves game speed when display and simulation rates differ; repeated world animation can still show judder.
- **Native 90 + render interpolation / stable HUD:** experimental high-Hz rendering with current HMD/input and one native tick of delayed world presentation above 90 Hz. Native local wheel/driver animation remains protected. 120/144 Hz can still miss cadence, reproject or judder.

Do not interpret a clean exit, zero submit errors or correct game speed as proof of smooth headset rendering. The latest owner 120 Hz report averaged about 102.4 render FPS with 90 Hz game logic; that is progress, not stable 120 certification. Keep OBS and AA in testing and use Feedback to review the timing summary. No headset-wide motion-smoothing/refresh settings are changed for you.

## Tested scope and known limits

The owner tested the preceding Photo build across 90/120 Hz with 12 entries and 65 PNGs, without reported entry/copy/PNG failures. A subsequent session recorded seven grip actions and three PNGs. The new default bordered 2D view, persistent labels, stereo viewfinder and Xbox shortcut default passed CPU/build checks but await physical headset/controller comparison. High-Hz visual acceptance remains incomplete. Touch/Quest, Steam Frame, Vive and other controller/wheel combinations remain physically untested here and require a compatible Windows SteamVR/OpenVR PC setup; no standalone headset port is included.

Occasional stalls, tracking/focus recovery and sustained high-Hz performance still need investigation. One 90 Hz run recorded a roughly 1.9-second world gap. True stereo character selection/garage, the model viewer, unrestricted spectator/chase tools, custom tracks and multiplayer remain outside the supported release scope.

Validation: actual desktop/native build; 74 native checks and 137 launcher checks passed; 117 Python checks passed. Two optional checks were skipped. CPU tests do not certify visual/GPU/controller acceptance. Binaries are unsigned; byte-for-byte source build reproducibility is not claimed.

## Install, update and roll back

Extract into a **new writable folder** and keep all package files together. Verify SHA-256 against SHA256SUMS.txt. Supply your own compatible raw NTSC-U retail disc BIN; no game data, personal saves or screenshots are distributed.

Keep the old installation, settings and saves backed up with the game closed. Selectively copy your own VR-Settings.ini, UI-Settings.ini, Launcher-Appearance.json and game/memcards, and reuse/import your own disc. Preserve any old game/captures folder separately. Keep new binaries, default config, bindings and manifests together. Copy Timing-Preview.json only if you deliberately want the previous timing profile; otherwise the clean install uses 90 Hz. Saves diverge between installations after playing. [v0.1.1 remains available](https://github.com/CR4zyHoBb1T52P1Ck/CTR-VR/releases/tag/v0.1.1) as the earlier fallback.

Feedback exports an allowlisted summary for your review and can open an editable GitHub issue draft. No raw logs/photos, identifiers, credentials or saves are uploaded automatically. Community evidence is reviewed with the project owner before action.

Thank you for playing, recording, testing and sharing feedback. [Support Devon](https://ko-fi.com/devdoesdevthings) · [Project and issues](https://github.com/CR4zyHoBb1T52P1Ck/CTR-VR)
