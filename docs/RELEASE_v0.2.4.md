# CTR VR v0.2.4 — PiP Menu Fix

Fixes the in-headset Picture-in-Picture menu appearing unresponsive when choosing
which recording view is large. **144 Hz remains experimental. Demanding tracks
and Creator recording can still slow down at 90/120 Hz; this is not a general
frame-rate or interpolation fix.**

## What changed

- **PiP large-view choices are visible immediately.** The old menu accepted A
  and directional input, but omitted the selected value from its label. It now
  displays **CHASE LARGE / HEADSET SMALL** or **HEADSET LARGE / CHASE SMALL**.
  Input handling and labels use the same capture-action classification.
- **A or Right opens Recording layout / PiP.** The compact page explains how to
  change choices and that recording output applies after resuming gameplay.
  Existing action IDs, bindings and saved choices are retained.
- **Feedback selects newly arrived sessions on refresh.** Deliberately selected
  historical sessions stay selected when the list is unchanged. Local session
  times, measured headset/native rate and a short report ID make repeated or
  incorrect exports easier to notice.
- **Better reviewed diagnostics.** Bounded launch/exit context records approved
  timing, capture, HUD/input enablement and saved AA choices. Session receipts
  identify the tested source/game rather than assuming the current installation.
  Missing reports, signed exits and conflicts stay explicit. OBS recording and
  video timestamps are optional player declarations.
- Full JSON export remains available; the GitHub button opens a compact reviewed
  draft, with manual attachment of the full report. There is no automatic upload,
  raw-log forwarding, GitHub token storage or report-to-code automation.
- Complete source includes offline comparison/triage, recovery fixtures and
  read-only audit/provenance tools. They add no render-loop logging overhead.

Driving input ownership, wheel calibration, motion bindings, force-feedback
behavior, Photo controls/looks, saved HUD placement, capture compositing and
timing algorithms are retained. Photo/freecam, the loaded-kart viewer, Chase and
the broader supported features remain as documented in the v0.2.3 release.

## Use the PiP menu

1. Enable the **CTR VR Capture** window and choose **Chase** in Creator settings.
2. In VR Settings, open **Creator / Capture > Recording layout / PiP** with A or
   Right. Up/Down selects a row; Left/Right or A changes its value.
3. Choose a visible inset corner (Bottom left or Top left), then the large view.
   The label immediately shows the saved choice. Back returns to Creator;
   B closes settings.
4. Resume gameplay and check the separate window titled **CTR VR Capture**.
   The headset and its normal mirror keep their gameplay camera. Paused/loading
   output uses the existing panel path, so it is not a live Chase-layout preview.
5. In OBS, capture **CTR VR Capture** rather than the main game/SteamVR mirror.

The headset-eye image includes its HUD/status whether it is large or small.
Main recording HUD/status controls apply independently to the mono/Chase view.
Saved PNGs remain under **game/Captures** in the installation that created them.

## Refresh rates and remaining limits

- **90 Hz:** default/reference. Use a 90 Hz headset mode for the baseline option.
  Creator recording and demanding races can still cause dips.
- **80 Hz:** owner-tested fallback with the current Native option.
- **120 Hz:** select **CURRENT: Native — 80 / 90 / 120 owner-tested**, set the
  headset to 120 Hz before launch, and restart the game after a refresh change.
  Effective native rate is matched at launch; the saved in-game FPS value need
  not be rewritten. Owner testing includes OBS and AA, but heavier workloads can
  still run below full game speed.
- **72 Hz** remains physically untested. **144 Hz remains EXPERIMENTAL**, including
  race cadence/slowdown limitations. Native clock recovery and older interpolation
  choices are explicitly experimental/legacy; recovery is not a guarantee of
  smooth full-rate world rendering.

PiP menu operation and swapped recording output have owner confirmation. One
healthy 120 Hz Relic Challenge run does not certify the earlier AI-race workload.
Compare the same race mode, track, capture layout, OBS and AA settings before
attributing a performance change. Start/end snapshots are not continuous telemetry.
Current-clip animated viewer playback and broadly compatible controller profiles
retain their existing experimental/physical-test limits.

## Install, preserve and build

Download **ctr-vr-v0.2.4-windows-x86.zip** and extract to a **new writable folder**.
Verify it against **SHA256SUMS.txt**, keep its binaries/manifests/bindings/defaults
together, then open **CTR VR Launcher.exe**. Supply your own compatible raw NTSC-U
disc BIN. The download includes no retail data, personal settings, saves, captures
or private development history.

Keep the old installation as rollback. With the game and launchers closed, back
up and selectively transfer your own memory cards/settings; keep the new package's
runtime files and manifests. Do not overwrite the old working folder or mix a
lone executable with another release's files. Existing screenshots stay in the
installation where they were taken.

The named **ctr-vr-v0.2.4-source.zip** asset contains the complete corresponding
native/VR/launcher sources, pinned build inputs, licenses and build instructions.
GitHub's automatic source-code ZIP/TAR contains only the public documentation
repository. Follow the complete source archive's **BUILD-SOURCE.md**; retail data
is not needed for building/CPU tests. Matching source is supplied; byte-for-byte
build reproducibility is not claimed.

The game executable matches the owner-tested PiP menu candidate. The launcher
promotes the displayed release identity. Validation includes 40 timing/creator
checks, 88 native checks (one optional skipped), 207 launcher checks, the
reproduced menu-label regression and package/source integrity/privacy checks.
No additional headset performance result is inferred from CPU tests.
