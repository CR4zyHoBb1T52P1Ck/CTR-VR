# CTR VR v0.2.2 — Chase Camera & Picture-in-Picture

**A recording-only Chase camera with an optional first-person inset for OBS.**
The project owner confirmed the working output in video. **144 Hz remains
EXPERIMENTAL.** Use90 or native120 for normal comparison; this update does not
claim to solve full144 rendering or every hardware configuration.

## Start recording

1. With the game closed, open **CTR VR Launcher > Creator**. Enable the capture
   window, select **Chase camera — experimental**, choose recording resolution,
   30/60 update rate, FOV and recording HUD/status, then **Save Creator settings**.
2. For two views, set **Chase picture-in-picture: headset view** to **Bottom left**
   or **Top left**. **Off** keeps Chase alone. The paused VR Creator menu's framing
   row becomes **CHASE HEADSET INSET** when Chase is selected.
3. In OBS, add **Window Capture** and select the window titled **CTR VR Capture**.
   Alt+Tab to inspect it. **The main game window and SteamVR mirror still show
   your headset view.** Primary desktop mirror Capture rate only paces that
   headset preview; it does not select the recording camera.
4. Load a single-player hub/race. Chase supplies the main recording image. Your
   headset keeps its selected driving view and controls. The inset copies that
   headset eye: first person when you drive in first person. It does not force a
   gameplay camera change. The complete eye fits without stretching; bars may
   appear because its aspect differs from the landscape inset.

Capture and PiP default **OFF**; saved preferences are retained. Default
**Alt+F1** cycles recording views, **Alt+F2/F3** toggle recording HUD/status,
**Alt+F5** resets Chase while selected and **Alt+F12** saves the selected capture
as a PNG. Custom shortcut assignments remain respected. In Photo, Reset retains
its existing Photo camera behavior. Keep the main game window focused for keys.
PNGs save in **game/captures**; Launcher > Creator > Open screenshots opens it.

## What the mode does

- A fixed external camera sits3.2m behind and1.3m above the kart dashboard root
  (the root is0.45m above the kart), with bounded position/heading smoothing.
  Scene/level/scale changes, teleports, pause/Photo, mode changes and long or
  backward time gaps reset smoothing instead of dragging the camera across maps.
- A private renderer restores the captured chassis/driver hidden by first-person
  body settings and retains the separate native wheel sprites. It owns its
  geometry, sorting and camera; headset and Photo buffers are not replaced.
- Chase uses the existing one optional mono scene draw at30/60 capture cadence.
  PiP adds a colour copy and scissored border clear, **not another camera render**,
  new recording window or additional render target. Off performs no inset GL work.
- The inset is roughly30% of output width. It is composited into the recording
  and its PNG before readback. Photo, menus/loading, other views and Chase eye
  fallback do not receive an inset.
- Recording HUD/status toggles control the main mono view. The inset includes
  whatever HUD/status is visible in the headset. Hide the headset layout or turn
  PiP off when that inset must be HUD-free. Individual widget choices remain saved.

## Fallbacks and performance limits

The camera has **no wall collision/obstruction avoidance**. Walls can cover it,
and native captured visibility can omit scenery behind the player/camera. Wheels
remain rotating sprites rather than new3D models. When the native pose or required
captured body/wheel geometry is unavailable or incomplete, recording safely falls
back to the current eye. Pause/loading/menu output uses the current native panel.
A Chase GL failure latches its own eye fallback; restart to retry. Existing mirror
and other mono recording paths remain available.

The accepted144-Hz run recorded3,301 Chase world draws and2,734 PiP composites,
with zero capture errors. It also recorded411 Chase fallback frames. The latest
reject value was zero, so the summary does not identify each earlier fallback's
cause. These are call counters, not a guarantee of uninterrupted Chase or full
headset cadence.

That run averaged about**52.2 rendered world frames/s**, with mean native logic
about140.1 updates/s at a144 target. All76 measured render windows were below
target. **It confirms the feature's output, not stable144 performance.** It was
not the planned matched90/120 comparison. OBS and in-game AA remain the performance
target; neither is silently disabled. Compare the same track, capture preset,
HUD and mirror with PiP Off/On. Eye Fill/Fit remain the inexpensive fallback.

## Refresh setup and retained features

Close the game, set the actual headset refresh in SteamVR/connection software,
choose the matching launcher profile, **Save launch settings**, then Play. Restart
after a Hz change. The in-game FPS picker does not select headset Hz.

| Headset | Launcher choice | Status |
| --- | --- | --- |
|80Hz|Optimized native:72/80/90/120/144|Owner-tested lower-load fallback; available hardware modes vary.|
|90Hz|90Hz baseline|Preserved default and visual reference.|
|120Hz|Native120 tested optimized path, or Optimized native|Prior owner testing with OBS/AA; heavy tracks can still dip.|
|120/144 under load|Native120/144 clock recovery|Experimental speed recovery; visible cadence may remain lower. **144 remains experimental.**|

See the [complete refresh guide](https://github.com/CR4zyHoBb1T52P1Ck/CTR-VR/blob/main/docs/FRAME_RATE_GUIDE.md).
The v0.2.1 features remain: calibrated Index one/two-handed virtual-wheel driving,
physical-wheel steering and clutch reverse, hardware-gated wheel steering plus
motion gestures/button throws, gamepad directional items, input handoffs, optional
bounded default-Off force feedback/progressive pedals, personalized HUD, Photo
free camera/grip manipulation/looks/exact PNG framing, loaded frozen-kart viewer,
launcher customization and reviewed feedback. Read the
[full v0.2.1 feature catalog](https://github.com/CR4zyHoBb1T52P1Ck/CTR-VR/blob/main/docs/RELEASE_v0.2.1.md).
No driving bindings, ownership/recovery algorithms, Photo implementation, native
timing algorithm, AA defaults or native patch changed for Chase/PiP.

Quest/Touch, Steam Frame, Vive and other untested hardware remain compatibility
paths through Windows SteamVR/OpenVR, not standalone headset ports. Full-roster
animation, stereo frontend selection, custom tracks and multiplayer remain future
work. The old intermittent hub stall is not established globally fixed.

## Install, preserve and build

Download **ctr-vr-v0.2.2-windows-x86.zip**, verify SHA256SUMS.txt and extract to a
new writable folder. Keep the complete package together and import your own
compatible raw NTSC-U disc BIN. No retail data or personal saves are included.
Preserve the full previous installation. With game/launcher closed, copy your own
VR-Settings.ini, UI-Settings.ini, optional Launcher-Appearance.json and game/memcards;
re-import/reuse your disc and select/save timing for the actual headset. Keep the
new binaries, manifests, bindings, defaults and config together. Old screenshots
remain in the old game/captures. Roll back by opening the complete old folder.
**v0.2.1 and earlier releases remain available unchanged.**

**ctr-vr-v0.2.2-source.zip** supplies complete matching modified native source,
bridge, launcher/tooling, pinned SDK, vendored SDL and notices. GitHub automatic
source archives contain only the public documentation tree. Matching source is
supplied; byte-for-byte build reproducibility is not claimed. Launcher/tooling are
MIT; the native integration is GPL-3.0-or-later and dependencies retain their terms.

83 native,158 launcher and118 offline checks pass, with two optional skips.
Coverage includes actual inset compositing bounds/main-eye isolation, geometry,
camera resets, settings, cadence and existing input/Photo behavior. Runtime game
bytes match the owner's accepted Chase/PiP test. No game, OBS, SteamVR or motor was
automatically launched for release preparation. Feedback remains reviewed numeric
evidence with deliberate issue submission, not automatic uploads or code execution.

The next workblock will organize **Quick Access** around common Creator/Chase/PiP
actions while preserving existing calibration, HUD and mixed-controller access.
That menu change is intentionally not bundled into this accepted recording update.
