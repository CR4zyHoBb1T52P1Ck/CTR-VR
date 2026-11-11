# Theatre: controls and filming

Current PC recording workflow: pause the live PC VR game, open F9 settings,
then **Theatre / record race takes > Record take on resume**.
Resume using the controller; the take starts on the next safe live frame.
Pause to save the take and wait for SAVED. F7 is an optional keyboard start/stop.
Red REC means recording. OBS/Creator Capture video is separate. Quit normally, then use the
launcher Theatre library to open/edit the saved take. The live menu is not the
playback director. Photo now has a direct settings Home entry as well.

Capture on the PC, then direct a saved scene or moving take. Theatre playback
does not run the original race simulation. Missing off-camera objects/effects
and captured visibility limits can remain. Exports are silent H.264 MP4: 1280x720 landscape or 720x1280 portrait,
up to30minutes, with a30fps target; distinct-frame rate depends on workload.

## Start

Launcher > Theatre: select Desktop director or Tracked VR viewfinder, choose a
capture, then Open selected capture. Double-click uses that playback selection.
Tracked VR currently uses PC SteamVR streaming, not standalone Frame. It shows a
gold camera window in a dark VR room, not immersive course geometry.

Capture new take opens Play and starts the live PC VR game with recording armed.
After GO, use the paused settings Record take on resume button, or focus the game
and tap F7 to start/stop; Alt+F11 saves a frozen scene.
Wait for SAVED before closing. Pause, Photo, tracking loss and scene changes can
seal a take. The live REC indicator has its own HUD / Layout placement menu. Kart is the
default anchor; Head and World are optional. Select Grab REC badge for its frozen
laser editor; hold grip/trigger to place, stick up/down to size, then Done to save.

## Camera and tools

Action                    Keyboard/mouse             Gamepad                 Tracked Frame
Move                      WASD                       Left stick              Left stick
Look                      RMB drag / arrows          Right stick             Head or right stick
Down / up                 Q / E                      LB / RB                 LT / RT
Faster movement           Hold Shift                 D-pad speed             D-pad speed
Camera speed - / +        Minus / Equals             D-pad Down / Up         D-pad Down / Up
Zoom                      Mouse wheel                LT / RT                 Tools > Lens Zoom
Roll                      Z / C                      Hold L3 + right stick   Rotate grabbed camera
Aim at player             F                          R3                      Tools > Aim at Player
Reset camera              Home                       Tools > Reset Camera    Tools > Reset Camera
Player anchor / float     F4                         Y (tools closed)        Y (tools closed)
Hide/show editor          T                          View / Back             Left bumper
Open tools                Tab                        Menu / Start            Right stick click
Select / activate tool    Arrows / Enter             D-pad / A               D-pad or left stick / A
Close tools               Esc                        B                       B
Exit viewer               Esc with tools closed     Y with tools open       Y with tools open

In tracked VR, F5/left stick click switches Head/Handheld. Aim a cyan dot at the
gold window and squeeze either grip to grab. Release holds the shot. F6/Frame
right bumper resets the window into reach. Opening Tools parks the handheld
camera and brings tools into head view. An existing grip stays attached; closing
Tools resumes it without jumping. Releasing the grip inside Tools releases it.
Stick steering works alongside a grip and an idle connected gamepad. When both
devices steer the same axis, the gamepad takes that axis to avoid doubled motion.
Head and handheld modes retain the same clean export path.

Gamepad motion keeps its normal route when connected. Tracked buttons remain
available alongside it; duplicate commands are filtered per action. The newest
tracked Frame D-pad shortcuts need a hardware check. Index has its dedicated
profile; functions without a dedicated shortcut remain available in Tools.

## Playback, shots and recording

Action                    Keyboard                    Gamepad / tracked Frame
Play / pause              F3 or Space                X
Pause                     K                          B with tools closed
Previous / next frame     Comma / Period             D-pad Left / Right
Reverse / fast forward    J / L                      Tools > Reverse / Forward
Playback slower / faster  [ / ]                      Tools > Slower / Faster
Seek one second           PgDn / PgUp                Tools > Back / Ahead1Sec
Seek ten seconds          Shift+PgDn / Shift+PgUp    Tools > Back / Ahead10Sec
Start / end               Tools                      Tools > Start / End
Mark In / Out             I / O                      Tools > Mark In / Mark Out
Loop / clear range        P / U                      Tools > Loop / Clear Range
Record / stop clip        F10                        A with tools closed
Open clips folder         F11                        Tools > Open Clips
Save / load camera shot   F8 / F9                    Tools > Save Shot / Load Shot
Previous / next shot slot Shift+F12 / F12            Tools > Prev Slot / Next Slot

D-pad changes camera speed/frames with Tools closed, and selects tools while
Tools is open. Camera speed and playback speed are different. Frozen scenes have
no moving transport. Saved shots are source-specific; they do not change the take.
Tap left/right to step one captured frame; hold to keep scrubbing backward/forward.
While gripping, A records/stops, X plays/pauses and B pauses, without opening Tools.
A confirms a selection when Tools is open. Record/Stop is also available in Tools.

Clips exclude editor controls, the gold frame and aim dots. Wait for SAVED before
opening clips or exiting. Closing the SteamVR dashboard leaves playback paused;
release controls and press X/F3 to resume. T/View hides the editor without stopping
recording. To film the gold VR window itself, capture SteamVR's VR View with OBS.

Release checks still pending: tracked Frame face buttons/D-pad, fresh-install
game/Photo return, and a complete long-race capture/reopen/export round trip.

## Phone framing, pointer editing and bookmarks

Select **Phone portrait 9:16 - 720x1280** beside the Theatre playback selector before opening a take,
or use V / the top-left **16:9 WIDE / 9:16 PHONE** button to switch the clean film layout.
Portrait renders at720x1280 with the same vertical field of view and narrower
horizontal framing. It is not a stretched landscape image. The gold outline is
its exact preview boundary. Finish the current clip before changing format.
The scene is rendered once; the UI is composed into separate rails afterwards.
The exported MP4 contains neither the rails nor the gold border.

Camera/range and shot tools are on the left; playback/seek and VR tools are on
the right. Transport and timeline are below the picture. Information and format
controls are above it. T / gamepad View / Frame left bumper still hides all UI;
press it again to restore the rails. Hidden UI cannot receive pointer clicks.

In tracked VR, aim either cyan laser at a button and squeeze that hand's trigger
to click. Release before clicking again. Aim at the timeline and hold the trigger
to drag forward/backward. The trigger operates the UI while aimed there; it does
not also raise/lower the camera. Grips on the top title move/tilt the editor separately; grips on the film window
remain camera grabs. Reset viewfinder recentres both. Camera movement and
keyboard/gamepad shortcuts remain available with Tools closed. R3/Tab/Menu opens
button focus navigation; D-pad directions now follow the visible button positions,
A activates and B closes. Tools temporarily parks the held camera, as before.

**Bookmarks are separate from the In/Out export range.** Add up to64 with M or
**ADD MARK**, then use N / **PREV MARK** and H / **NEXT MARK** to jump between them.
Delete / **DELETE MARK** removes the bookmark at the current captured frame.
Adding an existing frame does not create a duplicate. Gold ticks show every
bookmark; the first16 also display numbers to avoid crowding. Frame/gamepad can
activate all marker tools through button focus, and VR triggers can click them.
Bookmarks save automatically in a separate source-identified .ctrmarks file in
Videos/CTR-VR/Director Projects and reload with the same take. Capture files and
old shot projects are never rewritten. A visible SAVE FAILED message means the
new marker exists only for the current session.

Acceptance needed for this candidate: pointer clicks/drags, portrait preview and
export framing, outer-rail readability, and grip/shortcut behavior on the headset.
CPU fixtures establish geometry/file contracts, not headset correctness.

## Photo and live Creator portrait

The launcher Creator/Capture page now has **Photo + recording framing**. Choose
**Phone portrait9:16**, then Save Creator settings or Play with those choices.
In-game, use F9 > Creator/Capture > **Photo/video framing**, or the same row in
Photo Scene/Looks. A/left/right changes it and auto-saves. This shared setting
applies to Photo PNGs, the Kart viewer's PNGs and every live CTR VR Capture view.
Theatre keeps its separate framing selector for independent clip composition.
While Photo is active, **Shift+V** switches wide/phone without losing the frozen
pose. Wait for a PNG to finish; a busy request is refused. Plain V still controls
viewer animation. The Photo controls below describe the current assignments.

The three quality presets become720x1280,900x1600 and1080x1920 in portrait,
with exactly the same pixel count as their landscape equivalents. Photo, Clean
Mono, Stabilized and Chase render the selected aspect directly. Eye Fill crops
the existing eye image; Eye Fit preserves it with bars. Portrait does not change
headset eye resolution, game timing, steering bindings, Photo grips or exits.
The Photo gold frame fits within the original vertical size; the legible help
panels stay outside it. PiP corners/free position, size, role swap and gold style
remain available, with portrait-aware placement diagrams.

In OBS, capture the **CTR VR Capture** window and use a9:16 canvas/output matching
the selected size. Cropping a landscape OBS source alone is not portrait mode.
The primary game/SteamVR mirror remains the headset view. Keep your existing OBS
and AA target settings when comparing. PNGs retain the current Photo look and
strength. Finish a requested screenshot before changing output size/framing.

Candidate acceptance still required: Photo portrait PNG/look, menu and controller
return; Chase+PiP in both role orders; Eye Fit/Fill; OBS portrait capture; landscape
return; and a short Theatre portrait export. No public promotion is implied.

## Photo and kart-viewer controls (separate from Theatre)

Photo freezes the loaded game scene and saves PNGs; Theatre edits completed takes
and exports silent MP4s. Creator Capture feeds the separate OBS window. Their
controls are deliberately described separately.

- Frame: right trigger PNG; right A orbit/free; right B return; right Y reset;
  right X focuses/hides tools. Left bumper down, right bumper up. D-pad left/right
  previous/next filter; down/up opacity. Stick clicks select preview and follow.
- Xbox/gamepad: X PNG, A orbit/free, B/Back return, Y reset, Start focuses/hides
  tools. LB down/RB up. D-pad filters/opacity as above. LS/RS clicks preview/follow.
- Keyboard: F1 focuses/hides tools; H hardware help. Space/F12 PNG; P frame/stereo;
  L lock/follow; Tab/Enter orbit/free outside tools. WASD moves; Q/E lowers/raises;
  arrows/RMB look; Page Up/Down distance; Minus/Equals lens. Shift+V wide/portrait.
  [ / ] previous/next look; comma/period opacity; O restores Original.
- Focused tools: either stick or arrows selects; A/Enter activates; left/right
  adjusts. B/Esc hides focused tools first, then returns from Photo outside focus.
  D-pad filters and bumper height remain active. Point/trigger or touch also works.
- Grip the Photo tools title to move/tilt; grip + stick resizes. Grip away from its
  title drags the world; two grips scale it. Hide/show retains panel placement for
  the current Photo entry. Panels and help stay out of PNGs and clean Creator output.

Looks: Original, Vibrant, Warm Postcard, Cool Dusk, Black & White, Sepia, Noir,
Soft Pastel, Night Vision and Neon Arcade. Opacity blends back to Original. These
looks apply to Photo/Viewer previews and PNGs; they do not grade live Creator
video or Theatre exports. Existing presets keep their IDs and saved selections.
