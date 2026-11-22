# Complete corresponding source

Download [ctr-vr-v0.3.1-source.zip](https://github.com/CR4zyHoBb1T52P1Ck/CTR-VR/releases/download/v0.3.1/ctr-vr-v0.3.1-source.zip)
from the same release as the Windows package. Verify its SHA-256 against the
release's SHA256SUMS.txt, extract the entire archive, and read BUILD-SOURCE.md.

It includes the modified Turbocharged native tree, VR integration, launcher,
required build inputs, OpenVR API source/headers/libraries, vendored SDL, license
notices and offline build instructions. Retail game data is not needed to build.
It contains no personal settings/saves or development Git history.

This repository's Git tree contains player documentation and release records.
GitHub's automatically generated "Source code (zip/tar.gz)" links archive only
that documentation tree. Use the named **ctr-vr-v0.3.1-source.zip** release asset
for the complete buildable source corresponding to the Windows download.

Launcher/tooling: MIT. Native integration: GPL-3.0-or-later. Dependencies retain
their own notices. See CREDITS-AND-LICENSES.md and the full source license texts.
Matching source is supplied; byte-for-byte build reproducibility is not claimed.

## Standalone Frame preview source

The [v0.3.2-frame-preview.1 release](https://github.com/CR4zyHoBb1T52P1Ck/CTR-VR/releases/tag/v0.3.2-frame-preview.1)
contains the separately named `ctr-vr-v0.3.2-frame-preview.1-source.zip`. It supplies
the exact 22c8fdfe integration snapshot, modified native inputs, Frame-conditional
adapter/header inputs, pinned SDK, licenses and an offline Win32/CPU-only build
script. The later unaccepted batching candidate is excluded. Integration snapshot
IDs refer to the code in the named archive, not commits in this documentation repo.
The stable v0.3.1 source and artifacts above remain unchanged.
