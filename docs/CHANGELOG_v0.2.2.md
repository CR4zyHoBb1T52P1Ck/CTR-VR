# CTR VR v0.2.2 — Chase Camera & Picture-in-Picture

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
