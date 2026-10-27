# CTR VR v0.2.2 — headset refresh and native game timing

**90 Hz is the default/reference. Native 120 has owner testing with OBS and in-game AA. 144 Hz remains experimental.** Normal game speed or a fast compositor does not establish full-rate world rendering.

## Set the rate before launch

1. Close the game. Set headset Hz in SteamVR or your PC streaming/connection software. Choose a mode actually exposed by your headset/transport. The launcher does not change those settings.
2. Open **CTR VR Launcher > Customize > Timing**, choose a profile below, then **Save launch settings**. Check the saved timing summary; changing the dropdown without saving does not apply it.
3. Play in VR. Keep the native game renderer at Native 3D and native game Mirror mode off. **Primary desktop mirror** is a separate optional preview. Startup/menu panels are normal; load a playable single-player world before assessing stereo.
4. Restart after changing headset Hz. The profile coordinates effective native game rate at startup and preserves saved FPS/calibration. The in-game FPS picker is not a headset refresh setting; do not select 240 during VR testing.

| Actual headset mode | Choose in Customize | What to expect |
| --- | --- | --- |
| **80 Hz** | **Optimized native: 72 / 80 / 90 / 120 / 144 Hz** | The native game follows 80. Earlier owner testing succeeded; use where available as a lower-load fallback. |
| **90 Hz** | **90 Hz baseline** | Preserved default/reference. Set the headset to 90 too; running a 90 game on an 80 headset can slow it. |
| **120 Hz** | **Native 120 — tested optimized path** | Requires a 120 headset. No fixed90 clock/interpolation. Owner-tested with OBS/AA; heavy tracks may still dip. **Optimized native** at120 uses the same native-rate HUD/handoff foundation. |
| **120 Hz, game speed slows under load** | **Native120/144 clock recovery** | Experimental complete-frame recovery at120. It helps game speed, but visible rendering may remain lower. |
| **144 Hz** | **Native120/144 clock recovery** | **EXPERIMENTAL.** Bounded native steps preserve time, without guaranteeing144 distinct rendered frames. Eligible race frames trim a redundant window presentation. Return to120/90 if visual cadence is poor. |

These profiles follow the headset; the dropdown does not switch it to a rate. Mismatch/refresh-change guards require a restart rather than silently changing physics. 72 is a compatibility preview requiring actual support. Quest and other headset paths remain physically untested; see QUEST_PC_VR.md.

## Legacy modes and diagnostics

**Match headset** retains the older matching path. **Fixed90** separates game steps and VR presentation. **Native90 + interpolation / stable HUD** attempts render smoothing above90. They remain advanced comparison experiments rather than the normal choice for native80/90/120. Local kart/driver and separate wheel sprites keep their native-animation safeguards. The broader rate list does not validate every device or configuration.

Recovery can preserve music/game speed while images repeat or reproject. Feedback game/logic rate and meanClockPermille describe simulation pace; meanAppMilliFps and renderUnderCadenceWindows describe rendered world cadence. Include visible judder, not just the final FPS sample. Display budgets are approximately12.5ms at80,11.11ms at90,8.33ms at120 and6.94ms at144.

The new144 optimization omits the final native window resolve/downsample/present only when a fully eligible VR world will replace it. Native scene drawing, required AA/VRAM packing, animation, input, HUD, VR eyes and Creator Capture remain. Startup, portals, pause, Photo, loading, rejected worlds and90/120 use original native presentation. `timing_nativeWindowPresentsSkipped` counts omitted passes. No physical full-144 improvement is claimed before comparison.

## OBS and capture cost

Keep OBS and in-game AA active in a representative test. Compare the **same active Creator view, resolution, capture rate, HUD and mirror setting**. Eye Fill/Fit copy an eye; Clean mono and experimental Stabilized forward add a scene render at capture cadence. Photo temporarily uses its composition view, so the last capture-mode value can describe Photo rather than the race. Primary mirror Capture rate/Dark reduces copies/swaps; leave that window open for keyboard focus. OBS preview adds separate overhead, not another native game simulation.

For an issue, export reviewed Feedback and include Hz/profile, track, Creator view/preset, OBS/AA and whether game/audio speed or only image smoothness changed. Do not reset calibration to diagnose timing. Preserve the complete old installation as rollback.
