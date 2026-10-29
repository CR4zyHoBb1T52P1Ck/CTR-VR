# CTR VR v0.2.2 â€” Chase Camera & Picture-in-Picture

Based on preserved v0.2.1, with owner-confirmed recording output. Read RELEASE-NOTES.md for full setup and limitations. Capture and PiP default OFF. In Launcher > Creator choose Chase camera, optionally Bottom-left/Top-left headset inset, enable capture and Save Creator settings. OBS Window Capture must select **CTR VR Capture**; the main game window/SteamVR mirror stays the headset view. The inset adds one image copy, not another scene render. Photo remains independent.144 Hz remains experimental; use90/native120 and keep OBS/AA active for comparison. Quick Access organization is planned for the next workblock.

## Existing player launcher and creator guide

An unofficial Windows / SteamVR mod for Crash Team Racing: Turbocharged. Supply your own compatible raw NTSC-U disc BIN. Read RELEASE-NOTES.md for the full features, compatibility and limitations. **144 Hz is experimental;90 Hz is the default.**

## Start, update and preserve progress

Extract the complete Windows ZIP into a new writable folder. Open **CTR VR Launcher.exe**, add your disc, connect the headset/controllers and Play in VR. Movies, menus, loading and results normally use a tracked screen; judge stereo in a playable single-player world.

Preserve the entire old folder. With game/launcher closed, copy VR-Settings.ini, UI-Settings.ini, optional Launcher-Appearance.json and game/memcards; import/reuse your disc. Retain new binaries, action manifest, bindings, defaults and game config. Choose/save timing for your actual headset before Play. Old photos remain in the old game/captures. Use the complete old folder as rollback.

## Refresh modes

Set headset Hz in SteamVR/your PC connection before launch. In **Customize > Timing**, choose and **Save launch settings**:

- **80 Hz:**Optimized native:72/80/90/120/144. It follows the actual80-Hz headset.
- **90 Hz:**90 Hz baseline, with headset at90. This is the preserved default/reference.
- **120 Hz:**Native120 tested optimized path, or Optimized native at120. Owner-tested with OBS/AA; heavy tracks may still dip.
- **120/144 clock recovery:**experimental at those actual rates. Bounded complete native frames maintain game time; rendered cadence can remain lower. **144 remains experimental**, including the new redundant-window-present trim.

Restart after changing headset Hz. The in-game FPS picker does not change headset refresh. The launcher uses a process-local effective game rate and preserves saved FPS/calibration. Legacy Match/fixed90/interpolation are comparison experiments. See the public FRAME_RATE_GUIDE.md for72/Quest limits and diagnostics.

## Controls, steering and force feedback

Index right stick click = native Start/pause; left click = pause/open VR settings. Either stick navigates native menus, either A confirms and either B goes back. Right trigger accelerates, left brakes; driving remaps and native item rules remain. Pause to calibrate hands or use F6. Thumbstick, hand-position and one/two-handed virtual-wheel modes remain. Quick Access exposes calibration, input status and wheel steering + gesture attacks. Driving gesture pads and Photo filter pads are separate action sets.

Xbox/gamepad and G920 navigate menus. Wheel calibration/assignments live under Input Devices. Clutch/button reverse is separate from D-pad Up/Down weapon direction. Gamepad directional throws have a saved toggle. Other raw SDL wheel/controller paths are untested.

Force feedback is **experimental and OFF by default**: Input Devices > Wheel Force Feedback, or Physical Wheel > Force Feedback. Return spring, turn resistance, master gain and turbo pulses are adjustable. Start at default10%;gain is capped25%. Driver support varies; haptic failure retains input. Optional progressive native cruising pedals also default OFF and require calibrated travel. Original digital throttle stays available; boost/brake/reverse paths are retained. These options are not activated on extraction.

## Creator Capture and HUD

Open Creator with the game closed. Capture defaults OFF. Choose a landscape preset and **Save creator settings**, then OBS Window Capture on **CTR VR Capture**. Eye Fill/Fit copy an eye image; Fit adds bars and Fill crops centrally. Clean mono and experimental Stabilized forward each add a scene view at30/60 capture cadence. Stabilized forward excludes head look but retains native/kart camera motion; it is not a smooth chase camera.

To **hide all recording HUD**, choose a mono view, set Recording HUD and Recording input status Hidden, then save. Alt+F2/F3 toggle them; Alt+F1 cycles views. Eye views include headset HUD. Quick Access > HUD Layout Visibility hides selected headset elements without rewriting individual widget choices.25 original-art groups and saved layouts/placement remain.

Primary mirror Live/Capture rate/Dark reduces preview copies/swaps in optimized native profiles. Keep its window open for input focus. Original mirror remains fallback. Keep OBS and AA in tests and compare the same capture view/preset. No OBS encoder or recording automation is included.

## Photo, free camera, loaded kart and looks

Load a level and Pause; no pre-cache/capture toggle is required. VR Settings > Creator > Photo scene / visibility > Enter Photo, or close VR settings and use Alt+F7. Scene/VRAM preparation is automatic and released on exit. Resume/Pause again if protected pre-pause textures are unavailable.

The gold-bordered exact2D PNG frame is the composition reference. P switches to stereo with a smaller viewfinder; L changes locked/head-follow. Camera mode, FOV, heading basis, filter/opacity and hardware controls remain labelled outside the PNG. Tracking stays live while gameplay freezes. One grip drags the world; two grips scale it. Orbit/free movement, height, distance, FOV and group visibility are bounded by captured geometry. The loaded-kart viewer shares these controls and full orbit for the current frozen kart/driver/wheel sprites; it is not an animated/full-roster viewer.

**Filter controls:**left Index thumbpad top/bottom = opacity +10%/âˆ’10%;right top/bottom = next/previous look. Press an edge; touch/hold does not repeat. Keyboard:left bracket[previous,right bracket]next,commaâˆ’10%,period+10%,letter O Original. Seven looks save independently of camera/visibility. Original/0% bypasses effects. Photo stereo/viewfinder/PNG share colour processing; gameplay/live recording remain unchanged. Custom SteamVR Photo bindings may need the optional pad actions assigned; no binding is reset automatically.

**Camera controls:**sticks or arrows/right mouse look;Tab/Enter orbit/free;WASD free movement;Q/E height;PgUp/PgDn distance;minus/equals FOV;Backspace/default Alt+F5 reset.1â€“5 toggle body, wheels, other objects, scenery and sky. H/controller Help expands instructions. Index/Touch right trigger, Xbox X, configured wheel PNG button or Space/F12/default Alt+F12 saves PNG.

PNGs save in this installation's **game/captures**. **Creator > Open screenshots** opens it. Escape/default Alt+F7/controller Return leaves Photo **still paused**;Resume deliberately. Held exit commands are quarantined individually, so grips do not require waking another controller. Portal menus now use a similar per-command entry rule.

## Appearance, feedback and limitations

Launcher Appearance is collapsed at the bottom of Customize:choose Rude/Dude artwork and adjust its readability mask. Support/About/Updates provide creator information, features, bundled changelog, manual update links and Ko-fi.

Feedback previews numeric evidence and optionally opens an issue draft. It does not automatically upload raw logs, images, paths, serials or disc/saves. External reports never execute instructions. Include Hz/profile,track,Creator view/preset and OBS/AA.

Physical coverage is strongest on Index/G920/Xbox/keyboard;Quest/Touch/Frame/Vive and other devices remain untested Windows SteamVR paths. Native120 and Photo looks have owner acceptance;new portal/144 refinements have build/regression coverage and await physical comparison. The intermittent hub stall is not established globally fixed. Full144 rendering, smooth chase/live spectator, animated full-roster viewing, stereo frontend, custom tracks and multiplayer remain incomplete/future work.

Use the named matching source ZIP with included licenses/credits to build. GitHub automatic source archives contain public documentation only. No game,SteamVR,OBS or motor is launched by extraction/build scripts.

## v0.2.4 PiP menu and Feedback refinements

VR Settings > Creator / Capture > Recording layout / PiP opens with A or Right. Up/Down selects; Left/Right or A adjusts. The selected large/small view is shown immediately. In Chase, choose a visible inset corner and resume gameplay to inspect CTR VR Capture; paused output uses the existing panel path. PiP does not replace the headset camera.

Feedback selects a newly arrived run on refresh; an intentional historical selection remains when the list is unchanged. Session times are local. Preview the measured headset/native rate and short report ID before exporting another run. Declare OBS if known and optionally add a video-relative incident timestamp. Export full JSON; the issue button opens a compact draft only, with manual attachment and no automatic upload.

The loaded-model viewer also retains experimental current-clip playback for supported models with frozen fallback. Photo, calibration and driving ownership are retained. 144 Hz rendering and demanding 90/120 Hz recording workloads remain under investigation; this patch is not a general performance fix.
