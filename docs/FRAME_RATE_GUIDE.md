# CTR VR v0.2.3 — headset refresh and native game timing

**90 Hz is the default/reference. Native 80/90/120 have owner testing; 120 was
tested with OBS and in-game AA. 144 Hz remains experimental.** Heavy tracks and
Creator capture can still dip. Correct game speed does not prove full-rate images.

## Set the rate before launch

1. Close the game. Set actual headset Hz in SteamVR or your PC connection software.
   Use a mode your headset/transport exposes; the launcher does not change it.
2. Open **Launcher > Customize > Headset timing**. Choose a profile and **Save
   launch settings**. Check the saved summary; restart after a headset Hz change.
3. Keep the native renderer at Native 3D and native game Mirror mode off. The
   optional Primary desktop mirror is separate. Load a playable world before
   assessing stereo; startup/menu panels are intentional.
4. The profile coordinates native game rate at startup and retains saved FPS and
   calibration. The in-game FPS picker does not set headset refresh. Do not
   independently choose 240 FPS during VR testing.

| Actual headset mode | Choose in Customize | Scope |
| --- | --- | --- |
|80 Hz|Current: Native|Earlier owner-tested lower-load fallback where available.|
|90 Hz|Current: 90 Hz reference|Preserved default/reference. Set the headset to 90 too.|
|90 Hz|Current: Native|Maintained native optimizations; retain this when comparing a previous native90 run.|
|120 Hz|Current: Native|Owner-tested with OBS + AA. Heavy races/recording can still slow.|
|120/144 Hz under load|Experimental: Native clock recovery|Bounded native steps preserve game time; visible rendering can remain lower.|
|144 Hz|Native or clock recovery|Experimental. Full144 race rendering is not established. Return to120/90 if cadence is poor.|
|72 Hz|Native|Compatibility path requiring hardware support; physical testing pending.|

## Current, experimental and legacy choices

Current identifies the maintained path, not certification on every track or device.
Experimental needs more validation. Legacy identifies an older comparison path.
Customize normally shows the 90 Hz reference, Native and experimental recovery.
**Show older / superseded timing experiments** reveals the rest. A saved legacy
selection remains visible and unchanged. Expanding that list never selects a mode.

Native uses the game's own rate-dependent timing and current HUD/handoff path,
without interpolation or catch-up. Recovery uses bounded additional complete
native frames at 120/144 when needed. It can keep music/game speed near real time
while images repeat or reproject. These are different models; compare the same
profile when evaluating only a Hz or capture-setting change.

Early Match headset, Fixed90, 90+interpolation, dedicated native120 and dedicated
native144 remain available for controlled comparisons. Interpolation has known
judder/object-matching limits and is not the preferred native80/90/120 path.
Mismatch/refresh-change guards require restart rather than changing physics
silently. Quest and other headset paths still need physical verification through
a compatible Windows SteamVR/OpenVR host; no standalone app is included.

## Recording cost and diagnostics

Keep OBS and native AA enabled in a representative test. Match track, active
Creator view, resolution, capture rate, FOV, HUD and primary mirror. Eye Fill/Fit
copy an existing eye; Clean mono, Stabilized and Chase add one world render at
capture cadence. PiP copies an existing image rather than another scene draw.
Swapping PiP adds copies and a small scratch target. Primary mirror Capture rate
or Dark reduces that optional preview's copies/swaps; keep the window open for
keyboard focus. OBS preview is separate overhead, not another game simulation.

The previous native90 capture setup/HUD optimization is active, but the latest
short run still averaged 86.08 rendered/logic FPS. It does not prove a regression
or improvement against longer runs. v0.2.3 adds presentation subphase counters to
separate context entry, image copy/flush, window swap and context restoration.
Do not add overlapping CPU scopes as independent frame-budget costs.

Feedback meanLogicMilliFps/meanClockPermille describe simulation pace;
meanAppMilliFps and renderUnderCadenceWindows describe rendered world cadence.
Include visible judder and audio/game speed, not just the final FPS sample.
Budgets are approximately 12.5 ms at80, 11.11 ms at90, 8.33 ms at120 and6.94 ms
at144. Complete game timing can be healthy while rendering misses those budgets.

The guarded144 pass can skip a redundant native window presentation in eligible
world frames. It preserves required drawing, AA/VRAM, animation, input, HUD, VR
eyes and Creator. Menus/Photo/loading/rejected worlds and90/120 keep original
native presentation. This is not a full144 performance acceptance claim.

For feedback include Hz, exact timing profile, track, Creator view/preset, OBS/AA,
and whether slowdown affected game speed or images. Don't reset calibration to
diagnose timing. Preserve the complete previous installation for rollback.
