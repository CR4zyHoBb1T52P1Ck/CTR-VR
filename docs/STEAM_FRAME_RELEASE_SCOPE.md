# Steam Frame: three separate modes

## PC streaming

Connect Frame to the Windows PC through SteamVR. The owner has accepted stock
gameplay and its Frame menu/face-button/directional-item fixes. The new Theatre
head camera, tracked grips, gamepad direction and clean clip exports have useful
owner results. Dedicated Frame Theatre face buttons and the newest D-pad shortcuts
still need their own check. Desktop Theatre is a separate Windows process.

## Local standalone flatscreen

The owner-tested local flatscreen installation runs the preserved v0.2.5 Windows
runtime through Proton on Frame's theatre screen. It has a separate Non-Steam
library entry/profile from experimental VR. It does not require PC streaming.
This is flatscreen play, not stereo VR and not the new PC Theatre application.

Local launch uses CTR_FLATSCREEN=1 with no VR argument or CTR_MOVING_VR variable.
Wheel acquisition/calibration remain off for this gamepad path. Keep profiles,
saves and Proton identities separate from the experimental VR installation.
Progress is copied during setup, not live-synchronized. Supply your own compatible
game data; no disc, personal memory card, device key or paired address is bundled.

The maintainer's paired-device install has been tested. A portable clean-user
setup bundle and fresh-install verification are still release work; this Windows
candidate does not install anything on a headset. Preserve the existing working
Frame entry. The optional turn-strength candidate has CPU coverage and remains
separate from the accepted original flatscreen runtime until tested.

## Local standalone VR

Private standalone VR boots and can race, but performance remains unsuitable for
supported play. Keep it experimental and in its own entry/profile. Headset reset,
runtime overrides, driver settings and global rendering changes are not part of
this release candidate. No native ARM port, locked80/90Hz or standalone Theatre
compatibility is claimed.
