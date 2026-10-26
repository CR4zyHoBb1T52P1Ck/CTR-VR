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
