# CTR VR v0.3.2-frame-preview.1 — Last Tested Standalone Frame Build

**22 November 2026 | Experimental standalone update | Hardware hiatus**

## A personal update from Devon

My Steam Frame has stopped charging. After an afternoon of troubleshooting, I
have contacted Valve support to work through a repair, replacement or possible
RMA. I do not have a confirmed resolution or a return date yet.

I am honestly really sad about this. We have spent a tremendous amount of time
getting CTR running locally on Frame, and the latest improvements were finally
making the standalone VR experience feel more stable. I wanted to keep pushing
this weekend, and I know some of you were looking forward to that too.

Before stepping away from the hardware, I wanted to share the **last build I
actually tested**. From my experience it is the best standalone Frame version we
have reached so far. It remains experimental: some of it is mostly playable,
particularly the previously tested flatscreen/theatre-screen path, while demanding
standalone VR races still have substantial frame-pacing and performance problems.
Please read the measured results and installation limits below before downloading.

**This will be the last standalone Steam Frame update for the foreseeable future.**
Standalone Frame testing and development are on hiatus until Valve and I can sort
out working hardware. There is no promised restart date, and an RMA has not yet
been confirmed. I am sorry to everyone who was hoping for a finished, smooth
standalone VR release right now. We got further than where we started, but we
have not finished the job, and I do not want to present an unfinished result as a
solved one.

I hope people can still enjoy what is already here, make some clips, race, explore,
and have fun with the mostly playable parts while this is paused. Thank you for
trying the mod, sharing feedback, supporting the work and spending time with me.
It really does mean a lot. <3

This does **not** mean every CTR VR feature or every other project is being
abandoned. I may reconnect my Index and continue PC VR acceptance or other work
that I can actually test. Those will be separate decisions and separate builds.
The hardware-dependent Frame work is paused; this post is not a promise of an
untested workaround or a schedule I cannot guarantee.

## Which download is this?

This is a **preview update overlay for an existing compatible standalone Frame /
Proton installation**. It is not a native SteamOS/ARM port, a complete game, a new
universal Frame installer, or a replacement for the stable PC package.

- **Frame preview overlay:** the exact last owner-tested Win32 game executable,
  current Frame/Theatre bindings, a reviewed launch-profile description, local
  profile/check tools, instructions, notices and checksums.
- **Complete corresponding source:** the exact integration source snapshot for
  that executable, the patched native source tree, required pinned OpenVR build
  inputs, license texts, an offline Windows source-build script and CPU test list.
- **PC/Index users:** keep using [v0.3.1 — Theatre and Creator Studio](https://github.com/CR4zyHoBb1T52P1Ck/CTR-VR/releases/tag/v0.3.1)
  unless you deliberately want to investigate the Frame branch. Its stable assets
  and the earlier releases remain unchanged.

The public Git repository contains release documentation and records. Download
the explicitly named source asset for the buildable integration; GitHub's automatic
Source code ZIP/TAR only contains the documentation repository.

The later **batched-culling candidate is not included**. It passed CPU checks, but
I did not complete a headset test before the hardware failure. Publishing that
instead would mean substituting an unaccepted experiment for the build I asked
to share. It remains preserved privately as future work.

## What the last full test actually showed

The final tested build completed a three-lap Cortex Castle run and shut down
cleanly. The sampled race windows report seven CPU opponents. The owner reported
a slightly steadier background and slightly less ghosting. Those observations
are useful acceptance feedback, not a claim that the presentation target was met.

| Measurement | Retained result |
| --- | --- |
| Headset / native simulation target | 72 Hz / 72 updates per second |
| Measured native logic average | 71.995 updates/s |
| Measured game-clock average | 100% |
| Submitted world stereo-pair average | 36.468 pairs/s |
| Eye targets | 2064 x 2064 per eye, 100% runtime scale |
| Sampled native AA setting | 6; configured AA retained |
| Opaque input vertices rejected outside both eyes | 64.52% |
| Opaque-culling fallbacks during this run | 0 |
| Valid sparse GPU timestamp samples | 61 of 61 retired samples |
| Reported Submit errors / captured-UI GL errors | 0 / 0 |
| Session end | Completed native shutdown and lifecycle cleanup |

**Game speed and display smoothness are different things.** The game clock is now
very close to the requested 72 Hz simulation rate, but the world presentation is
still around half that target in this demanding run. Repeated presentation,
judder, ghosting and uneven delivery can remain even when the music and kart
simulation feel correctly timed. This is not native 72 Hz standalone acceptance.

For context, the earlier locally collected mono-AA-off comparison averaged
37.295 submitted world pairs/s. The latest test used configured AA, so comparing
those two means does not isolate culling or AA performance. There is no supported
claim that this final test increased average FPS over that particular comparison.

The final sparse mean command-stream spans were about **8.898 ms native render**,
**9.429 ms stereo before submission**, with **2.083 ms HUD capture nested inside
the native span**. These timestamps include scheduling and possible command
starvation. They are not exclusive GPU execution costs, and the HUD number must
not be added to the native number as though it were a separate phase. Remote-play
footage also does not measure what was scanned out inside the headset.

72, 90 and 120 Hz remain optimization goals for standalone. They are not achieved
performance promises. Desktop/Index refresh acceptance from earlier releases
must not be reused as standalone Frame acceptance.

## Progress against the blockers

### 1. From startup failures to a complete standalone VR race

Early standalone work hit initialization refusals, crashes and inconsistent
adapter selection. We separated the problem into small native-adapter, pointer-
width, graphics-resource and eye-submission checks rather than treating every
failure as a game crash.

Adapter verification and isolated eye-submission diagnostics established that
Frame could select a real adapter and accept eye pairs. That did not automatically
make the game renderer work, but it removed a major uncertainty. Subsequent
resource/state fixes got the actual game into stereoscopic standalone VR and
allowed full races and hub traversal to be tested.

This build preserves that working path. It is still a Windows x86 executable
using the existing Proton/compatibility setup. We have not qualified every Frame,
firmware, Proton version, controller arrangement or clean installation.

### 2. Restoring current menus and controller access

An older standalone branch did not include the current interactive menu work.
That was a real regression: a fast build is not useful if the settings, Photo,
Theatre or controller navigation become inaccessible. The standalone source was
brought forward to include the newer feature/menu work, and the owner confirmed
the updated menus worked.

The sprint also addressed missing Frame face-button behavior, weak/incomplete
navigation paths, and directional-item controls. Shared controller paths cover
keyboard, gamepad and the applicable Frame input modes; tracked-controller paths
and gamepad emulation remain distinct. D-pad shortcuts are gated so hub/menu
navigation does not accidentally replicate race weapon actions or enter a race.
The owner specifically accepted the corrected hub D-pad behavior.

Flatscreen steering/turn-strength work and the separate flatscreen library path
were retained rather than sacrificing the accepted local theatre-screen option
while experimenting with VR. The older flatscreen acceptance is separate from a
new all-device acceptance of this final executable in every flat configuration.
Frame's own pointer/gamepad switching and system menus can still affect input.

### 3. Matching simulation to the headset without masking the problem

Some early performance experiments made the game feel too slow. Later changes
restored game speed but produced severe world/shadow/racer judder, uneven jumps
or an accelerated feel. Interpolation and pose-smoothing experiments were not
accepted as a substitute for solid native-rate rendering.

The published profile keeps the headset-matched **raw simulation clock** and
leaves frame interpolation and experimental pose smoothing **off**. It retains
the measured near-72 Hz game logic from the final run. There is no automatic
claim that choosing a higher headset refresh makes the hardware render enough
new world frames to match it.

We have not claimed every jump, collision or long-session timing edge case is
universally fixed. The distinction is explicit: timing improved substantially;
presentation still needs work.

### 4. Avoiding redundant native work while preserving framebuffer behavior

The renderer does more than draw two stereo world pictures. Native rendering,
PSX-style framebuffer/material behavior, menus, HUD replay, capture tools and
state restoration all share the graphics context. Blindly deleting the native
pass or caching state globally can break visual effects, Photo or menus.

The retained profile uses guarded native-render coalescing and bounded upload /
vertex-storage reuse, scoped raster/framebuffer/matrix/scalar/projection/material
state reuse, and split-setup reuse. HUD work uses a scoped dispatch path with
explicit restore/invalidation boundaries. These are attempts to avoid repeated
work inside known ownership scopes, not assumptions that graphics state stays
unchanged across unrelated game, Photo or menu operations.

Whole-program Win32 Release optimization, O2 and SSE2 are also part of the tested
build configuration. This is not a debug executable accidentally being used for
performance testing.

Some experiments were deliberately left off. Scalar-group reuse caused a crash
in an earlier candidate. Broader world batching did not establish useful merges
in the retained measurements. The associative precision-cache experiment did
not establish a delivered benefit, and the final profile uses the reference
precision path. Texture-state caching and abandoned batching paths are not
silently enabled just because their source remains available for research.

### 5. Removing off-screen opaque geometry

The existing ordered/transparent pass already had conservative visibility
checks, but the main opaque pass still submitted the entire world/object stream
to both eyes. The final tested optimization added bounds for contiguous groups
of 64 triangles and rejects a group only when it is outside **both** current eye
views.

It preserves triangle order, material/depth policy, sky rendering and the ordered
pass. It uses side planes only, with the existing conservative margin, to avoid
incorrectly removing depth-biased PSX materials. Local kart transforms, uncertain
bounds, interpolation, invalid views and mismatched geometry retain fail-open
drawing. Static track bounds are cached until world replacement; moving-object
bounds update with the live stream.

The final run rejected 64.52% of opaque input vertices without a recorded culling
fallback. That is a concrete reduction in submitted geometry, but it still left
about 45.15 surviving opaque draw ranges per eye. Median world-eye CPU time was
2.1965 ms. Reducing that submission overhead was the next investigation; the
later multi-draw/sibling-eye-reuse candidate remains untested and is excluded.

### 6. Preserving visual quality while exposing the real cost

The tested profile retains 100% runtime eye scale and configured AA. The final
reported targets were 2064-square per eye. Resolution and AA were not quietly
reduced to obtain the final culling result.

Foveated **Sharpening** can improve perceived clarity on Frame; it is not the same
as foveated rendering and does not establish a reduced shading workload. The
owner's renderpass-optimization experiment produced a blank result and was not
made a requirement or default. Broad visual/quality switches are not treated as
free optimizations when they remove rendering or change framebuffer behavior.

Pixelation, moving-object ghosting and uneven frame delivery were recurring
blockers. Earlier crate/sign positioning issues were addressed and the owner
reported them improved. The latest build felt a little steadier, but remaining
presentation artifacts and the insufficient world-frame rate are still release
limitations, not cosmetic issues we can declare solved.

### 7. Making failures and performance self-reporting

A large part of this effort was building evidence that survives real testing:
startup logs, progress checkpoints, a final report, launch/executable/session
association, lifecycle stages, native workload counters, CPU phase distributions
and sparse GPU command-stream timestamps.

Collectors retain partial evidence when Steam Stop prevents a final report.
Missing final output is not automatically called a crash. Collection validates
report paths and launch/runtime feature delivery, and archived comparison reports
can be read without launching the game. GPU samples have ownership, availability,
retirement, capacity and pairing checks. Zero or unavailable measurements are not
automatically labelled success.

Interactive sessions remain under player control: no automatic test deadline or
watchdog shutdown is required by this profile. Reports and settings stay local;
this release contains no support credentials, pairing keys, private logs, retail
game data or personal saves.

### 8. Keeping Photo, Theatre and Creator work usable

The established v0.3.1 feature set remains available separately: interactive
Photo/Viewer panels, grabbable placement, pointer/hover help, controller-friendly
Theatre take recording and browsing, free/player cameras, head/hand-tracked
filming tools, timeline scrubbing and shot/range/bookmark tools, wide/portrait
Photo and video workflows, and Creator Chase/PiP output for OBS.

The Frame branch incorporates the newer menu/tool foundations, and their CPU
regressions are part of the release checks. Capture location handling targets
**Desktop/CTR VR CAPTURES**, with **Photos**, **Videos** and **Race Takes** folders.
Photo encoding and capture were previous blockers; the directory/writer fixes
and CPU checks do not amount to a new full end-to-end acceptance of every capture
mode on Frame. VR rendering, capture encoding and recording at once can still
cost substantial resources.

Theatre takes retain observed visual draws; they are not a deterministic
simulation replay with complete unseen objects, full effects or recorded game
audio. Portrait output and filming features should not be described as a complete
replay engine or as guaranteed full-rate video export on standalone hardware.

### 9. Custom tracks and per-eye DLSS: real progress, separate unfinished work

Sunken Sprint and the custom-track work progressed from scene rendering and
transparency fixes into native driving, crates and item interaction prototypes,
Turbo, dropped TNT/Nitro, collision/blast/splash and scene/replay work. Lap/finish/
retry, recovery/save handling and bot/model allocation/rollback have dedicated
integration and regression work. That does not make a complete eight-racer,
audio/animation-complete custom championship an accepted public feature. Those
private prototypes are not bundled as a finished custom race in this release.

Per-eye DLSS research progressed through adapter checks, stereo texture/depth /
bias transport, Win32 GL to x64 helper transfers, real two-eye NGX diagnostic
evaluations on the desktop NVIDIA system, captured native-source evaluation,
persistent helper/channel work, runtime-size selection and refusal/cleanup tests.
These removed several important interoperability uncertainties.

However, successful diagnostic evaluation is not accepted live gameplay DLSS.
Motion/history validity, live resource ownership, typed/core GL-D3D interoperability,
correct per-eye output and gameplay fallback remain distinct integration gates.
The most recent core export diagnostic had a failure to investigate. This Frame
release contains **no enabled live DLSS feature**, no claimed DLSS speedup, and no
bundled proprietary NGX/DLSS runtime. Desktop NVIDIA experiments must not be
presented as standalone Frame support. Complete Garage, multiplayer and broader
roadmap systems also remain unfinished.

## Install, preserve progress and roll back

Read **INSTALL-FRAME.md** in the overlay before copying files. Start from an
existing compatible standalone installation or prepare your own compatible base
with the stable package and your own legally supplied game data. A first-time
universal Frame installer has not been qualified.

Close CTR before changing files. Back up your current executable and input files,
settings, saves and captures. Keep the old installation or a verified executable
backup. Do not overwrite personal configuration with somebody else's settings.
Copy the overlay's game files only into the intended game's directory. If using
the Windows launcher to prepare data, do that before the overlay; its stable
package manifest is not a manifest for this Frame preview. Launch the preview
directly through the separate standalone Steam entry and the supplied profile.

The launch-profile helper prints settings/options and checks files; it does not
register Steam entries, install Proton, start SteamVR or launch the game. Verify
SHA256SUMS.txt and the release manifest. Use your existing tested compatibility
configuration and keep flatscreen and VR entries separate.

For rollback, restore your own pre-update executable/bindings/profile with the
game closed, or return to your retained stable installation. Nothing here removes
v0.3.1 or changes its assets. Do not put retail game data or private diagnostics in
public issue attachments without reviewing what you are sharing.

## Verification, provenance and the remaining limits

The published executable is the exact tested **c190a0d727f6f9dca2b5f503fe10f850918f6abbc5d51094d7cdec9324f93b4b**
build from integration source **22c8fdfea5728532fd120b3b7da369b18286ae27**.

The preparation retained 59 CPU suites and 10,938 opaque-drawing checks, plus
feature-delivery, report-boundary, restore, folder/input preservation and public
source checks. The final release includes a separate clean source-build report;
that report states what was actually compiled and tested. CPU tests do not prove
headset comfort, another user's Proton environment, locked framerate or every
Photo/Theatre/track interaction. Byte-for-byte rebuild reproducibility is not
claimed; the distributed tested binary remains unchanged.

Known limits remain: demanding standalone VR races below target presentation;
judder/ghosting and workload-dependent delivery; incomplete first-install and
broader-controller qualification; resource-heavy recording/capture; unfinished
custom full-race/Garage/multiplayer systems; and no accepted live per-eye DLSS.
There will be no new Frame hardware acceptance while the headset is unavailable.

This is a free, unofficial project, unaffiliated with Valve, the original game's
owners or the Turbocharged maintainers. Native integration is GPL-3.0-or-later;
launcher/tooling and dependencies retain their own license terms. Full notices
and corresponding source are provided. No retail game data is distributed.

Thank you again for playing, supporting, making videos, sharing feedback and
having fun with me. I am sorry this particular sprint has ended on a hardware
problem. I hope this preserved build gives you something worth enjoying while
we wait to see what support can do.

[Project](https://github.com/CR4zyHoBb1T52P1Ck/CTR-VR) ·
[Stable v0.3.1](https://github.com/CR4zyHoBb1T52P1Ck/CTR-VR/releases/tag/v0.3.1) ·
[Support Devon](https://ko-fi.com/devdoesdevthings)
